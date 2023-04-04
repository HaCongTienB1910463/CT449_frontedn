<template>
    <div class="page">
        <ContactForm @submit:contact="createContact" @createContact:contact="createContact" />
        <p>{{ message }}</p>
    </div>
    <form>
        <div class="form-group">
            <label for="exampleInputEmail1">Email address</label>
            <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp"
                placeholder="Enter email">
            <small id="emailHelp" class="form-text text-muted">We'll never share your email with anyone else.</small>
        </div>
        <div class="form-group">
            <label for="exampleInputPassword1">Password</label>
            <input type="password" minlength="8" class="form-control" id="exampleInputPassword1" placeholder="Password">
        </div>
        <div class="form-check">
            <input type="checkbox" class="form-check-input" id="exampleCheck1">
            <label class="form-check-label" for="exampleCheck1">Check me out</label>
        </div>
        <button type="submit" class="btn btn-primary">Sign In</button>
    </form>
</template>
<script>
import ContactService from "@/services/contact.service";
import ContactList from "@/components/ContactList.vue";
import axios from 'axios';
</script>