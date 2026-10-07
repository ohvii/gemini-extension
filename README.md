<img src="assets/icon.png" alt="Ohvii" width="96" height="96">

# Ohvii for Gemini CLI

<!-- approved-about:start -->
Buy a California home through the AI you already use. Research homes, compare sales and review disclosures, then prepare offers and counters. Generate purchase agreements, addenda and repair requests, and track deadlines with guidance through closing. You choose the terms, review documents, sign securely and approve delivery.
<!-- approved-about:end -->

## Connect

Gemini CLI currently requires a Gemini Code Assist Standard or Enterprise license, or a paid Gemini / Gemini Enterprise Agent Platform API key. Google moved consumer access, including free accounts and Google AI Pro/Ultra, to **Antigravity CLI** on June 18, 2026. See [Google's account guidance](https://developers.googleblog.com/an-important-update-transitioning-gemini-cli-to-antigravity-cli/). A personal Google sign-in alone does not establish Gemini CLI access.

This package targets Gemini CLI. Antigravity uses a separate plugin format; an Ohvii Antigravity package and native connection have not yet been verified.

Install [Gemini CLI](https://geminicli.com/docs/get-started/installation/), then install Ohvii:

```sh
gemini extensions install https://github.com/ohvii/gemini-extension
gemini
```

Review the extension's requested access. Authenticate using your supported Gemini CLI license or paid API method. In the Gemini CLI conversation, run:

```text
/mcp auth ohvii
/mcp list
```

Sign in to your Ohvii account in the browser, review the requested permissions and approve the connection. Return to Gemini CLI and confirm that Ohvii is connected. If you installed the extension while Gemini CLI was already running, restart that session first.

Your Gemini authentication powers the AI; your separate Ohvii sign-in connects your saved homes and purchase records. Never paste tokens, cookies or authorization codes into a conversation. No API key or static bearer header is needed for Ohvii.

The extension automatically loads the shared buyer workflow in `GEMINI.md`. It connects directly to the hosted Ohvii service over Streamable HTTP and uses OAuth discovery. It contains no executable hooks, local server, credentials or buyer records. Use a current Gemini CLI release with remote MCP OAuth support.

## Start a conversation

<!-- approved-prompts:start -->
- “Help me find homes that fit my budget and what I’m looking for.”
- “Compare recent sales so I can decide what to offer for this home.”
- “Review this home’s disclosures, explain the risks, and help me plan inspections or repair requests.”
- “Help me prepare an offer for this home.”
- “Help me evaluate this counteroffer and prepare a response.”
- “What do I need to complete before closing, and what’s due next?”
<!-- approved-prompts:end -->

Use the connected account's current records. Transaction support is for self-represented California buyers. You choose the terms, review documents, sign securely and separately approve delivery. Signing and other buyer-only steps open a focused Ohvii browser handoff; return to the conversation after completing the step so Gemini can check the saved result. Ohvii does not move money or act as your licensed buyer's agent.

This extension uses structured tools and browser handoffs. It does not claim inline MCP App rendering or install an app into the consumer Gemini website or mobile app.

## Updates and access

```sh
gemini extensions update ohvii
```

Restart Gemini CLI after an update. To remove the extension:

```sh
gemini extensions uninstall ohvii
```

Revoke the connection in Ohvii's connected-agent settings when you want to withdraw access. Uninstalling locally does not revoke the server-side grant.

OAuth permissions cover workspace, research and document reads, document uploads, workspace edits, offer confirmation, communications sending and transaction confirmation. Each action remains subject to Ohvii's review, signing and approval requirements. Your AI provider receives information used in the conversation under its own terms.

## Support and license

- [Ohvii](https://ohvii.com)
- [Connection and tool reference](https://ohvii.com/developers)
- [Support](https://ohvii.com/support)
- [Privacy](https://ohvii.com/privacy)
- [Terms](https://ohvii.com/terms)

The connector configuration, buyer workflow and documentation use the [MIT license](LICENSE). The hosted application, backend and buyer data are outside this source release. The [artwork notice](assets/NOTICE.md) covers the bundled Ohvii logo.
