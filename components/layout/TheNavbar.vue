<script setup lang="ts">
import { CircleUser, Menu, Package2, Search } from 'lucide-vue-next'
import { Button } from '@/components/ui/button'
import { Input } from '@/components/ui/input'
import { Sheet, SheetContent, SheetTrigger } from '@/components/ui/sheet'
import {
  DropdownMenu,
  DropdownMenuContent,
  DropdownMenuItem,
  DropdownMenuLabel,
  DropdownMenuSeparator,
  DropdownMenuTrigger,
} from '~/components/ui/dropdown-menu'
</script>

<template>
  <header class="sticky top-0 h-16 flex items-center gap-4 border-b bg-background px-4 md:px-6">
    <nav class="hidden flex-col gap-6 text-lg font-medium md:flex md:flex-row md:items-center lg:gap-6 md:gap-5 md:text-sm">
      <a
        href="#"
        class="flex items-center gap-2 text-lg font-semibold md:text-base"
      >
        <Package2 class="h-6 w-6" />
        <span class="sr-only">Acme Inc</span>
      </a>
      <a
        href="#"
        class="text-foreground transition-colors hover:text-foreground"
      >
        Dashboard
      </a>
      <a
        href="#"
        class="text-muted-foreground transition-colors hover:text-foreground"
      >
        Orders
      </a>
      <a
        href="#"
        class="text-muted-foreground transition-colors hover:text-foreground"
      >
        Products
      </a>
      <a
        href="#"
        class="text-muted-foreground transition-colors hover:text-foreground"
      >
        Customers
      </a>
      <a
        href="#"
        class="text-muted-foreground transition-colors hover:text-foreground"
      >
        Analytics
      </a>
    </nav>
    <Sheet>
      <SheetTrigger as-child>
        <Button
          variant="outline"
          size="icon"
          class="shrink-0 md:hidden"
        >
          <Menu class="h-5 w-5" />
          <span class="sr-only">Toggle navigation menu</span>
        </Button>
      </SheetTrigger>
      <SheetContent side="left">
        <nav class="grid gap-6 text-lg font-medium">
          <a
            href="#"
            class="flex items-center gap-2 text-lg font-semibold"
          >
            <Package2 class="h-6 w-6" />
            <span class="sr-only">Acme Inc</span>
          </a>
          <a href="#" class="hover:text-foreground">
            Dashboard
          </a>
          <a
            href="#"
            class="text-muted-foreground hover:text-foreground"
          >
            Orders
          </a>
          <a
            href="#"
            class="text-muted-foreground hover:text-foreground"
          >
            Products
          </a>
          <a
            href="#"
            class="text-muted-foreground hover:text-foreground"
          >
            Customers
          </a>
          <a
            href="#"
            class="text-muted-foreground hover:text-foreground"
          >
            Analytics
          </a>
        </nav>
      </SheetContent>
    </Sheet>
    <div class="w-full flex items-center gap-4 md:ml-auto lg:gap-4 md:gap-2">
      <form class="ml-auto flex-1 sm:flex-initial">
        <div class="relative">
          <Search class="absolute left-2.5 top-2.5 h-4 w-4 text-muted-foreground" />
          <Input
            type="search"
            placeholder="Search products..."
            class="pl-8 lg:w-[300px] md:w-[200px] sm:w-[300px]"
          />
        </div>
      </form>
      <DarkToggle />
      <DropdownMenu>
        <DropdownMenuTrigger as-child>
          <Button variant="secondary" size="icon" class="rounded-full">
            <CircleUser class="h-5 w-5" />
            <span class="sr-only">Toggle user menu</span>
          </Button>
        </DropdownMenuTrigger>
        <DropdownMenuContent align="end">
          <DropdownMenuLabel>My Account</DropdownMenuLabel>
          <DropdownMenuSeparator />
          <DropdownMenuItem>Settings</DropdownMenuItem>
          <DropdownMenuItem>Support</DropdownMenuItem>
          <DropdownMenuSeparator />
          <DropdownMenuItem>Logout</DropdownMenuItem>
        </DropdownMenuContent>
      </DropdownMenu>
    </div>
  </header>
</template>

<style scoped>

</style>
