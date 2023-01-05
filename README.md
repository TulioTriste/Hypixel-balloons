# Hypixel-balloons

This is a first try code, im too busy to continue

```Java
Player player = (Player) sender;

Entity zombie = player.getWorld().spawnEntity(player.getLocation(),
    new GiantZombie(((CraftWorld) player.getLocation().getWorld()).getHandle()).getBukkitEntity().getType());

zombie.setCustomName("CustomZombie");
zombie.setCustomNameVisible(false);

LivingEntity entity = (LivingEntity) zombie;

entity.addPotionEffect(new PotionEffect(PotionEffectType.INVISIBILITY, Integer.MAX_VALUE, 1));

entity.getEquipment().setItemInHand(new ItemBuilder(Material.DIAMOND_BLOCK).build());

Block block = player.getLocation().getBlock();
block.setType(Material.FENCE);
block.getState().update();

Entity leashHitch = player.getLocation().getWorld().spawnEntity(player.getLocation(), EntityType.LEASH_HITCH);
entity.setLeashHolder(leashHitch);
```
