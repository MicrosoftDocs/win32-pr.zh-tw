---
title: D1103 洩漏的控制碼
ms.assetid: 9bb08cd6-104a-4168-b14e-3caec1679388
description: 已建立介面，但未發行。
keywords:
- D1103 洩漏的控制碼 Direct2D
topic_type:
- apiref
api_name:
- D1103 Leaked Handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: cc4b4e43f94bd4ceb5d7a2518879c69bd3ecf8f3
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/27/2021
ms.locfileid: "106993699"
---
# <a name="d1103-leaked-handle"></a><span data-ttu-id="653aa-104">D1103：洩漏的控制碼</span><span class="sxs-lookup"><span data-stu-id="653aa-104">D1103: Leaked Handle</span></span>

<span data-ttu-id="653aa-105">\[  \] 已建立介面介面，但未發行。</span><span class="sxs-lookup"><span data-stu-id="653aa-105">An interface \[*interface*\] was created but not released.</span></span>

## <a name="placeholders"></a><span data-ttu-id="653aa-106">預留位置</span><span class="sxs-lookup"><span data-stu-id="653aa-106">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="653aa-107"><span id="interface"></span><span id="INTERFACE"></span>*介面*</span><span class="sxs-lookup"><span data-stu-id="653aa-107"><span id="interface"></span><span id="INTERFACE"></span>*interface*</span></span>
</dt> <dd>

<span data-ttu-id="653aa-108">介面的位址。</span><span class="sxs-lookup"><span data-stu-id="653aa-108">The address of the interface.</span></span>

</dd> </dl> 




 

## <a name="possible-causes"></a><span data-ttu-id="653aa-109">可能的原因</span><span class="sxs-lookup"><span data-stu-id="653aa-109">Possible Causes</span></span>

<span data-ttu-id="653aa-110">不正確資源使用量。</span><span class="sxs-lookup"><span data-stu-id="653aa-110">Invalid resource usage.</span></span> <span data-ttu-id="653aa-111">應用程式無法在不再使用某個介面時釋出該介面。</span><span class="sxs-lookup"><span data-stu-id="653aa-111">An application fails to release an interface when it is no longer in use.</span></span>

 

 




