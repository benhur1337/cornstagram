<script>
    const tempPosts = [1,2,3,4,5,6,7,8,9]
</script>

<div class="flex flex-row justify-evenly gap-6 p-6">
    <div class="h-[100px] w-[100px] bg-gray-500 rounded-full">

    </div>
    <div class="flex flex-col gap-2">
        <b>@user.name <button class="font-normal text-white bg-sky-500 p-2 rounded ml-2">Follow</button></b>
        <p>User bio over here</p>
    </div>
</div>

<div class="flex flex-row flex-wrap gap-4 justify-center p-6">
    {#each tempPosts as post}
        <div class="h-[100px] w-[30%] bg-gray-500 rounded-lg">{post}</div>
    {/each}
</div>