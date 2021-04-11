---
description: '執行緒環境區塊 (調試附注) '
ms.assetid: 5040CB82-D32F-4C44-8C03-30238D5B897A
title: '執行緒環境區塊 (調試附注) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d66b04b522bed8bdf7f5a5571c300019e4537b5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847303"
---
# <a name="thread-environment-block-debugging-notes"></a><span data-ttu-id="a0c42-103">執行緒環境區塊 (調試附注) </span><span class="sxs-lookup"><span data-stu-id="a0c42-103">Thread Environment Block (Debugging Notes)</span></span>

<span data-ttu-id="a0c42-104">執行緒環境區塊 ([**TEB 結構**](/windows/win32/api/winternl/ns-winternl-teb)) 保存執行緒的內容資訊。</span><span class="sxs-lookup"><span data-stu-id="a0c42-104">The Thread Environment Block ([**TEB structure**](/windows/win32/api/winternl/ns-winternl-teb)) holds context information for a thread.</span></span>

<span data-ttu-id="a0c42-105">在下列版本的 Windows 中，64位 TEB 內32位 TEB 位址的位移是0。</span><span class="sxs-lookup"><span data-stu-id="a0c42-105">In the following versions of Windows, the offset of the 32-bit TEB address within the 64-bit TEB is 0.</span></span> <span data-ttu-id="a0c42-106">這可以用來直接存取 WOW64 執行緒的32位 TEB。</span><span class="sxs-lookup"><span data-stu-id="a0c42-106">This can be used to directly access the 32-bit TEB of a WOW64 thread.</span></span> <span data-ttu-id="a0c42-107">在較新版本的 Windows 中，這可能會變更</span><span class="sxs-lookup"><span data-stu-id="a0c42-107">This might change in later versions of Windows</span></span>



|               |                        |
|---------------|------------------------|
| <span data-ttu-id="a0c42-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a0c42-108">Windows Vista</span></span> | <span data-ttu-id="a0c42-109">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a0c42-109">Windows Server 2008</span></span>    |
| <span data-ttu-id="a0c42-110">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a0c42-110">Windows 7</span></span>     | <span data-ttu-id="a0c42-111">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a0c42-111">Windows Server 2008 R2</span></span> |
| <span data-ttu-id="a0c42-112">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a0c42-112">Windows 8</span></span>     | <span data-ttu-id="a0c42-113">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a0c42-113">Windows Server 2012</span></span>    |
| <span data-ttu-id="a0c42-114">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a0c42-114">Windows 8.1</span></span>   | <span data-ttu-id="a0c42-115">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a0c42-115">Windows Server 2012 R2</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a0c42-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="a0c42-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0c42-117">偵錯結構</span><span class="sxs-lookup"><span data-stu-id="a0c42-117">Debugging Structures</span></span>](debugging-structures.md)
</dt> <dt>

[<span data-ttu-id="a0c42-118">**WOW64 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="a0c42-118">**WOW64\_CONTEXT**</span></span>](/windows/desktop/api/WinNT/ns-winnt-wow64_context)
</dt> </dl>

 

 
