# SEvcDemo
  This one-pager was the beginning. The goal now is to make the stack useful beyond a personal lab — turning self-hosted infrastructure into something   
  that produces real value.                                                                                                                              
                                                                                                                                                         
  What it is                                                                                                                                             
                                                                                                                                                         
  A single-machine Docker Compose stack running a complete sovereign layer: Bitcoin full node, Lightning (Alby Hub + LNbits), Nostr relay (strfry), media
   storage (Blossom), key management (Signet NIP-46 bunker), automated Nostr publishing (Storybot), Tor onion endpoints, and self-hosted mail.         
                                                                                                                                                         
  Everything talks to everything. No third-party APIs for core functions. One docker compose up -d runs the whole thing.                                 
              
  How it works                                                                                                                                           
                                                                                                                                                       
  - Bitcoin Core validates the chain locally. Alby Hub manages channels, LNbits exposes payment APIs.                                                    
  - strfry stores and relays Nostr events. Blossom handles media uploads to decentralized blob storage.                                                
  - Signet holds all Nostr keys in a NIP-46 bunker — applications sign remotely, keys never leave the host.                                              
  - Storybot runs a daily automated publishing pipeline for the 600BillionCWO Nostr identity: story generation, image handling, Blossom upload, timed    
  publishing at 4:20 UTC.                                                                                                                                
  - OpenClaw (AI agent gateway) orchestrates everything: cron jobs, Telegram integration, multi-model LLM routing, tool execution — all wired into the   
  sovereign stack.                                                                                                                                       
  - Tor bridges provide inbound access without exposing the host IP.                                                                                   
  - Tailscale mesh connects all management UIs. Nothing is exposed to the public internet.                                                               
                                                                                                                                                         
  What comes next
                                                                                                                                                         
  - noDNS — DNS over Nostr. npub-based domains resolved via signed DNS record events, served from a clearnet nameserver on bimbeam.at.                   
  - Making the stack reachable and useful for others, not just the operator.
  - Building real applications on top of the infrastructure that already runs.                                                                           
                                                                                       
