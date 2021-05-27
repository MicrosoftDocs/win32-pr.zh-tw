---
description: '執行緒環境區塊 (調試附注) '
ms.assetid: 5040CB82-D32F-4C44-8C03-30238D5B897A
title: '執行緒環境區塊 (調試附注) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9397c2d442b09b308c4886c2672e3be58b661c
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550583"
---
# <a name="thread-environment-block-debugging-notes"></a><span data-ttu-id="5af31-103">執行緒環境區塊 (調試附注) </span><span class="sxs-lookup"><span data-stu-id="5af31-103">Thread Environment Block (Debugging Notes)</span></span>

<span data-ttu-id="5af31-104">執行緒環境區塊 ([**TEB 結構**](/windows/win32/api/winternl/ns-winternl-teb)) 保存執行緒的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="5af31-104">The Thread Environment Block ([**TEB structure**](/windows/win32/api/winternl/ns-winternl-teb)) holds context information for a thread.</span></span>

<span data-ttu-id="5af31-105">在下列版本的 Windows 中，64位 TEB 內32位 TEB 位址的位移是0。</span><span class="sxs-lookup"><span data-stu-id="5af31-105">In the following versions of Windows, the offset of the 32-bit TEB address within the 64-bit TEB is 0.</span></span> <span data-ttu-id="5af31-106">這可以用來直接存取 WOW64 執行緒的32位 TEB。</span><span class="sxs-lookup"><span data-stu-id="5af31-106">This can be used to directly access the 32-bit TEB of a WOW64 thread.</span></span> <span data-ttu-id="5af31-107">在較新版本的 Windows 中，這可能會變更</span><span class="sxs-lookup"><span data-stu-id="5af31-107">This might change in later versions of Windows</span></span>



|  <span data-ttu-id="5af31-108">平台</span><span class="sxs-lookup"><span data-stu-id="5af31-108">Platform</span></span>     | <span data-ttu-id="5af31-109">版本</span><span class="sxs-lookup"><span data-stu-id="5af31-109">Version</span></span>                |
|---------------|------------------------|
| <span data-ttu-id="5af31-110">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5af31-110">Windows Vista</span></span> | <span data-ttu-id="5af31-111">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5af31-111">Windows Server 2008</span></span>    |
| <span data-ttu-id="5af31-112">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5af31-112">Windows 7</span></span>     | <span data-ttu-id="5af31-113">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5af31-113">Windows Server 2008 R2</span></span> |
| <span data-ttu-id="5af31-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="5af31-114">Windows 8</span></span>     | <span data-ttu-id="5af31-115">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5af31-115">Windows Server 2012</span></span>    |
| <span data-ttu-id="5af31-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5af31-116">Windows 8.1</span></span>   | <span data-ttu-id="5af31-117">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="5af31-117">Windows Server 2012 R2</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="5af31-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="5af31-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5af31-119">偵錯結構</span><span class="sxs-lookup"><span data-stu-id="5af31-119">Debugging Structures</span></span>](debugging-structures.md)
</dt> <dt>

[<span data-ttu-id="5af31-120">**WOW64 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="5af31-120">**WOW64\_CONTEXT**</span></span>](/windows/desktop/api/WinNT/ns-winnt-wow64_context)
</dt> </dl>

 

 
