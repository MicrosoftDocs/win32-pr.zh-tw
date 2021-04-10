---
description: 本附錄說明 Simplec 和 Simples 範例應用程式的重寫版本，可正常處理 IPv4 或 IPv6。已啟用 IPv6 的用戶端 CodeIPv6-Enabled Server 程式碼
ms.assetid: ffcbd59e-63ea-4df3-9db9-e7d4634eefeb
title: 附錄 B： IP 版本中立的原始程式碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 333e344376695122ebcd650ebf2595d70afbf7ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848028"
---
# <a name="appendix-b-ip-version-agnostic-source-code"></a><span data-ttu-id="501cd-103">附錄 B： IP 版本中立的原始程式碼</span><span class="sxs-lookup"><span data-stu-id="501cd-103">Appendix B: IP-version Agnostic Source Code</span></span>

<span data-ttu-id="501cd-104">本附錄說明 Simplec 和 Simples 範例應用程式的重寫版本，可正常地處理 IPv4 或 IPv6。</span><span class="sxs-lookup"><span data-stu-id="501cd-104">This appendix illustrates a rewritten version of the Simplec.c and Simples.c sample applications that gracefully handles either IPv4 or IPv6.</span></span>

-   [<span data-ttu-id="501cd-105">啟用 IPv6 的用戶端程式代碼</span><span class="sxs-lookup"><span data-stu-id="501cd-105">IPv6-Enabled Client Code</span></span>](ipv6-enabled-client-code-2.md)
-   [<span data-ttu-id="501cd-106">啟用 IPv6 的伺服器程式碼</span><span class="sxs-lookup"><span data-stu-id="501cd-106">IPv6-Enabled Server Code</span></span>](ipv6-enabled-server-code-2.md)

<span data-ttu-id="501cd-107">這段程式碼會」舉例說明此 IPv6 指南中所述的指導方針，並納入其中以提供已成功修改的原始程式碼，以新增 IPv6 支援。</span><span class="sxs-lookup"><span data-stu-id="501cd-107">This code exemplifies the guidelines set forth in this IPv6 guide, and is included to provide source code that has been successfully modified to add support for IPv6.</span></span> <span data-ttu-id="501cd-108">這個範例是刻意簡單的，但提供流覽和審查的實際操作範例。</span><span class="sxs-lookup"><span data-stu-id="501cd-108">This sample is intentionally simple, but provides a hands-on sample for perusing and reviewing.</span></span> <span data-ttu-id="501cd-109">[附錄 A：僅限 ipv4 的原始程式碼](appendix-a-ipv4-only-source-code-2.md)中提供此原始程式碼的 IPv4 版本。</span><span class="sxs-lookup"><span data-stu-id="501cd-109">An IPv4 only version of this source code is provided in [Appendix A: IPv4-only Source Code](appendix-a-ipv4-only-source-code-2.md).</span></span>

<span data-ttu-id="501cd-110">藉由比較附錄 A 中的原始程式碼 (僅限 IPv4) 和附錄 B (與 IP 版本無關) ，您可以瞭解修改 Windows 通訊端應用程式以新增 IPv6 支援所需的變更。</span><span class="sxs-lookup"><span data-stu-id="501cd-110">By comparing the source code in Appendix A (IPv4 only) and Appendix B (IP-version agnostic), you get a sense of the changes necessary to modify your Windows Sockets application to add support for IPv6.</span></span>

 

 



