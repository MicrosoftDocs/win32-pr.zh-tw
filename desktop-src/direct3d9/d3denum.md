---
description: 驅動程式功能旗標。
ms.assetid: 78ff4433-f0b5-4bbb-b2c0-bd389fbc31ce
title: D3DENUM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 059c2f9f1bf32275423bb9f2a9f484c12824bcda
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971132"
---
# <a name="d3denum"></a><span data-ttu-id="e25c4-103">D3DENUM</span><span class="sxs-lookup"><span data-stu-id="e25c4-103">D3DENUM</span></span>

<span data-ttu-id="e25c4-104">驅動程式功能旗標。</span><span class="sxs-lookup"><span data-stu-id="e25c4-104">Driver capability flag.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e25c4-105">#定義</span><span class="sxs-lookup"><span data-stu-id="e25c4-105">#define</span></span></td>
<td><span data-ttu-id="e25c4-106">值</span><span class="sxs-lookup"><span data-stu-id="e25c4-106">Value</span></span></td>
<td><span data-ttu-id="e25c4-107">描述</span><span class="sxs-lookup"><span data-stu-id="e25c4-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e25c4-108">D3DENUM_WHQL_LEVEL</span><span class="sxs-lookup"><span data-stu-id="e25c4-108">D3DENUM_WHQL_LEVEL</span></span></td>
<td><span data-ttu-id="e25c4-109">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="e25c4-109">0x00000002L</span></span></td>
<td><span data-ttu-id="e25c4-110">Microsoft Windows 硬體品質實驗室 (的 WHQL) 驅動程式測試。</span><span class="sxs-lookup"><span data-stu-id="e25c4-110">Microsoft Windows Hardware Quality Labs (WHQL) driver testing.</span></span> <span data-ttu-id="e25c4-111">這是一項耗時的測試，需要一秒或兩秒的時間才會受到影響。</span><span class="sxs-lookup"><span data-stu-id="e25c4-111">This is a time-consuming test requiring a one-second or two-second time penalty.</span></span> <span data-ttu-id="e25c4-112"><a href="d3dadapter-identifier9.md"><strong>D3DADAPTER_IDENTIFIER9</strong></a>的 WHQLLevel 成員會使用這個常數。</span><span class="sxs-lookup"><span data-stu-id="e25c4-112">This constant is used by the WHQLLevel member of <a href="d3dadapter-identifier9.md"><strong>D3DADAPTER_IDENTIFIER9</strong></a>.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e25c4-113">Direct3D 9 與 Direct3D 9Ex 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="e25c4-113">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="e25c4-114">在 Windows Vista、Windows Server 2008、Windows 7 和 Windows Server 2008 R2 上執行的 Direct3D9Ex 已淘汰 D3DENUM_WHQL_LEVEL， (或更新的作業系統) 。</span><span class="sxs-lookup"><span data-stu-id="e25c4-114">D3DENUM_WHQL_LEVEL is deprecated for Direct3D9Ex running on Windows Vista, Windows Server 2008, Windows 7, and Windows Server 2008 R2 (or more current operating system).</span></span> <span data-ttu-id="e25c4-115">其中任何一個作業系統都會針對 WHQL 等級傳回1，而不會檢查驅動程式的狀態。</span><span class="sxs-lookup"><span data-stu-id="e25c4-115">Any of these operating systems return 1 for the WHQL level without checking the status of the driver.</span></span> <br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="constant-information"></a><span data-ttu-id="e25c4-116">常數資訊</span><span class="sxs-lookup"><span data-stu-id="e25c4-116">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="e25c4-117">標頭</span><span class="sxs-lookup"><span data-stu-id="e25c4-117">Header</span></span>                   | <span data-ttu-id="e25c4-118">d3d9。h</span><span class="sxs-lookup"><span data-stu-id="e25c4-118">d3d9.h</span></span>     |
| <span data-ttu-id="e25c4-119">最低作業系統</span><span class="sxs-lookup"><span data-stu-id="e25c4-119">Minimum operating system</span></span> | <span data-ttu-id="e25c4-120">Windows 98</span><span class="sxs-lookup"><span data-stu-id="e25c4-120">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e25c4-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="e25c4-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e25c4-122">Direct3D 常數</span><span class="sxs-lookup"><span data-stu-id="e25c4-122">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




