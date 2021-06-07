---
description: 登錄是階層式資料庫，包含對 Windows 作業以及在 Windows 上執行的應用程式和服務而言很重要的資料。
ms.assetid: 4ed60563-73d8-4134-8cb2-8388734fb18d
title: 登錄的結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bf104806b5e4e10b4be7387018e714a0db8bf37
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386667"
---
# <a name="structure-of-the-registry"></a><span data-ttu-id="a3e3a-103">登錄的結構</span><span class="sxs-lookup"><span data-stu-id="a3e3a-103">Structure of the Registry</span></span>

<span data-ttu-id="a3e3a-104">登錄是階層式資料庫，包含對 Windows 作業以及在 Windows 上執行的應用程式和服務而言很重要的資料。</span><span class="sxs-lookup"><span data-stu-id="a3e3a-104">The registry is a hierarchical database that contains data that is critical for the operation of Windows and the applications and services that run on Windows.</span></span> <span data-ttu-id="a3e3a-105">資料是以樹狀結構格式進行結構化。</span><span class="sxs-lookup"><span data-stu-id="a3e3a-105">The data is structured in a tree format.</span></span> <span data-ttu-id="a3e3a-106">樹狀結構中的每個節點稱為索引 *鍵*。</span><span class="sxs-lookup"><span data-stu-id="a3e3a-106">Each node in the tree is called a *key*.</span></span> <span data-ttu-id="a3e3a-107">每個金鑰都可以同時包含子機 *碼和名* 為 *值* 的資料項目。</span><span class="sxs-lookup"><span data-stu-id="a3e3a-107">Each key can contain both *subkeys* and data entries called *values*.</span></span> <span data-ttu-id="a3e3a-108">有時候，索引鍵的存在就是應用程式所需的所有資料。有時候，應用程式會開啟金鑰，並使用與索引鍵相關聯的值。</span><span class="sxs-lookup"><span data-stu-id="a3e3a-108">Sometimes, the presence of a key is all the data that an application requires; other times, an application opens a key and uses the values associated with the key.</span></span> <span data-ttu-id="a3e3a-109">索引鍵可以有任意數目的值，而值可以是任何形式。</span><span class="sxs-lookup"><span data-stu-id="a3e3a-109">A key can have any number of values, and the values can be in any form.</span></span> <span data-ttu-id="a3e3a-110">如需詳細資訊，請參閱登錄 [數值型別](registry-value-types.md) 和登錄 [元素大小限制](registry-element-size-limits.md)。</span><span class="sxs-lookup"><span data-stu-id="a3e3a-110">For more information, see [Registry Value Types](registry-value-types.md) and [Registry Element Size Limits](registry-element-size-limits.md).</span></span>

<span data-ttu-id="a3e3a-111">每個金鑰都有一個名稱，其中包含一個或多個可列印字元。</span><span class="sxs-lookup"><span data-stu-id="a3e3a-111">Each key has a name consisting of one or more printable characters.</span></span> <span data-ttu-id="a3e3a-112">索引鍵名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a3e3a-112">Key names are not case sensitive.</span></span> <span data-ttu-id="a3e3a-113">索引鍵名稱不能包含反斜線字元 (\\) ，但可以使用任何其他可列印字元。</span><span class="sxs-lookup"><span data-stu-id="a3e3a-113">Key names cannot include the backslash character (\\), but any other printable character can be used.</span></span> <span data-ttu-id="a3e3a-114">值名稱和資料可以包含反斜線字元。</span><span class="sxs-lookup"><span data-stu-id="a3e3a-114">Value names and data can include the backslash character.</span></span>

<span data-ttu-id="a3e3a-115">每個子機碼的名稱都是唯一的，與階層中緊接在其上的金鑰有關。</span><span class="sxs-lookup"><span data-stu-id="a3e3a-115">The name of each subkey is unique with respect to the key that is immediately above it in the hierarchy.</span></span> <span data-ttu-id="a3e3a-116">索引鍵名稱不會當地語系化為其他語言，雖然值可能為。</span><span class="sxs-lookup"><span data-stu-id="a3e3a-116">Key names are not localized into other languages, although values may be.</span></span>

<span data-ttu-id="a3e3a-117">下圖是登錄編輯程式所顯示的範例登錄機碼結構。</span><span class="sxs-lookup"><span data-stu-id="a3e3a-117">The following illustration is an example registry key structure as displayed by the Registry Editor.</span></span>

![[登錄編輯程式] 視窗](images/regtree.png)

<span data-ttu-id="a3e3a-119">**我的電腦** 下的每個樹狀結構都是索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a3e3a-119">Each of the trees under **My Computer** is a key.</span></span> <span data-ttu-id="a3e3a-120">**HKEY \_ 本機 \_ 電腦** 金鑰具有下列子機碼：**硬體**、 **SAM**、**安全性**、**軟體** 和 **系統**。</span><span class="sxs-lookup"><span data-stu-id="a3e3a-120">The **HKEY\_LOCAL\_MACHINE** key has the following subkeys: **HARDWARE**, **SAM**, **SECURITY**, **SOFTWARE**, and **SYSTEM**.</span></span> <span data-ttu-id="a3e3a-121">每個金鑰接著都會有子機碼。</span><span class="sxs-lookup"><span data-stu-id="a3e3a-121">Each of these keys in turn has subkeys.</span></span> <span data-ttu-id="a3e3a-122">例如， **硬體** 金鑰具有子機碼 **DESCRIPTION**、 **DEVICEMAP** 和 **windows.applicationmodel.resources.core.resourcemap**; **DEVICEMAP** 索引鍵有數個子機碼，包含 **影片**。</span><span class="sxs-lookup"><span data-stu-id="a3e3a-122">For example, the **HARDWARE** key has the subkeys **DESCRIPTION**, **DEVICEMAP**, and **RESOURCEMAP**; the **DEVICEMAP** key has several subkeys including **VIDEO**.</span></span>

<span data-ttu-id="a3e3a-123">每個值都包含值名稱及其相關聯的資料（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="a3e3a-123">Each value consists of a value name and its associated data, if any.</span></span> <span data-ttu-id="a3e3a-124">**MaxObjectNumber** 和 **VgaCompatible** 是包含 **影片** 子機碼下之資料的值。</span><span class="sxs-lookup"><span data-stu-id="a3e3a-124">**MaxObjectNumber** and **VgaCompatible** are values that contain data under the **VIDEO** subkey.</span></span>

<span data-ttu-id="a3e3a-125">登錄樹狀目錄可以是深512層級。</span><span class="sxs-lookup"><span data-stu-id="a3e3a-125">A registry tree can be 512 levels deep.</span></span> <span data-ttu-id="a3e3a-126">您可以透過單一登入 API 呼叫，一次最多建立32個層級。</span><span class="sxs-lookup"><span data-stu-id="a3e3a-126">You can create up to 32 levels at a time through a single registry API call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3e3a-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="a3e3a-127">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a3e3a-128">[Windows 登錄簡介](/previous-versions/windows/it-pro/windows-server-2003/cc781906(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="a3e3a-128">[Overview of the Windows Registry](/previous-versions/windows/it-pro/windows-server-2003/cc781906(v=ws.10))</span></span>
</dt> </dl>

 

 
