---
title: D1101 未知的控制碼
ms.assetid: ae40058a-ea17-4262-87dc-0ce852c16c2a
description: 未由此 DLL 配置的介面傳遞給它。
keywords:
- D1101 未知的控制碼 Direct2D
topic_type:
- apiref
api_name:
- D1101 Unknown Handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 2a87491a02d3dea992f8dd767ad34cf83b2cbf40
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/27/2021
ms.locfileid: "106994928"
---
# <a name="d1101-unknown-handle"></a><span data-ttu-id="29917-104">D1101：未知的控制碼</span><span class="sxs-lookup"><span data-stu-id="29917-104">D1101: Unknown Handle</span></span>

<span data-ttu-id="29917-105">未由此 DLL 配置的介面 \[ *介面* \] 傳遞給它。</span><span class="sxs-lookup"><span data-stu-id="29917-105">An interface \[*interface*\] not allocated by this DLL was passed to it.</span></span>

## <a name="placeholders"></a><span data-ttu-id="29917-106">預留位置</span><span class="sxs-lookup"><span data-stu-id="29917-106">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="29917-107"><span id="interface"></span><span id="INTERFACE"></span>*介面*</span><span class="sxs-lookup"><span data-stu-id="29917-107"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="29917-108">介面的位址。</span><span class="sxs-lookup"><span data-stu-id="29917-108">The address of the interface.</span></span>

</dd> </dl> 




 

## <a name="possible-causes"></a><span data-ttu-id="29917-109">可能的原因</span><span class="sxs-lookup"><span data-stu-id="29917-109">Possible Causes</span></span>

<span data-ttu-id="29917-110">不正確資源使用量。</span><span class="sxs-lookup"><span data-stu-id="29917-110">Invalid resource usage.</span></span> <span data-ttu-id="29917-111">在 Direct2D 之外建立的資源會與 Direct2D factory 搭配使用，或在一個 factory 上建立的資源會與另一個 factory 建立的資源搭配使用。</span><span class="sxs-lookup"><span data-stu-id="29917-111">The resource created outside of Direct2D is used with a Direct2D factory, or the resources created on one factory was used with a resource created by another factory.</span></span>

 

 




