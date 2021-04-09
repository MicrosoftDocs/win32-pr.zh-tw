---
title: D1102 太多開啟的控制碼
ms.assetid: a7e52926-a4e6-4030-9e90-9df2b3e3edde
description: 找到大量的未發行介面。 目前此 DLL 配置了未發行介面。
keywords:
- D1102 太多開啟的控制碼 Direct2D
topic_type:
- apiref
api_name:
- D1102 Too Many Opened Handles
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: e3c12c2e2a7b47535e830c6ed65a828a16672bbf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678235"
---
# <a name="d1102-too-many-opened-handles"></a><span data-ttu-id="6dc13-105">D1102：太多開啟的控制碼</span><span class="sxs-lookup"><span data-stu-id="6dc13-105">D1102: Too Many Opened Handles</span></span>

<span data-ttu-id="6dc13-106">找到大量的未發行介面。</span><span class="sxs-lookup"><span data-stu-id="6dc13-106">A large number of unreleased interfaces were found.</span></span> <span data-ttu-id="6dc13-107">目前此 DLL 配置了 \[ *數目* 的 \] 未發行介面。</span><span class="sxs-lookup"><span data-stu-id="6dc13-107">Currently there are \[*number*\] unreleased interfaces allocated by this DLL.</span></span>

## <a name="placeholders"></a><span data-ttu-id="6dc13-108">預留位置</span><span class="sxs-lookup"><span data-stu-id="6dc13-108">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="6dc13-109"><span id="number"></span><span id="NUMBER"></span>*數量*</span><span class="sxs-lookup"><span data-stu-id="6dc13-109"><span id="number"></span><span id="NUMBER"></span>*number*</span></span>
</dt> <dd>

<span data-ttu-id="6dc13-110">由此 DLL 配置的未發行介面數目。</span><span class="sxs-lookup"><span data-stu-id="6dc13-110">The number of unreleased interfaces allocated by this DLL.</span></span>

</dd> </dl> 

|             |         |
|-------------|---------|
| <span data-ttu-id="6dc13-111">錯誤層級</span><span class="sxs-lookup"><span data-stu-id="6dc13-111">Error Level</span></span> | <span data-ttu-id="6dc13-112">警告</span><span class="sxs-lookup"><span data-stu-id="6dc13-112">Warning</span></span> |



 

## <a name="possible-causes"></a><span data-ttu-id="6dc13-113">可能的原因</span><span class="sxs-lookup"><span data-stu-id="6dc13-113">Possible Causes</span></span>

<span data-ttu-id="6dc13-114">已建立大量的資源。</span><span class="sxs-lookup"><span data-stu-id="6dc13-114">A large number of resources were created.</span></span> <span data-ttu-id="6dc13-115">雖然 Direct2D 的可用資源數量沒有上限 (但記憶體) 除外，但在遇到1001的即時物件、2001即時物件或3001的即時物件等時，debug 層會發出這項參考用訊息，因為這可能表示應用程式中發生流失。</span><span class="sxs-lookup"><span data-stu-id="6dc13-115">Although Direct2D has no upper bound on the number of available resources (except memory), the debug layer issues this informational message when it encounters 1001 live objects, 2001 live objects, or 3001 live objects etc, because this might indicate a leak in the application.</span></span>

 

 




