---
title: DevicePair 轉譯器屬性
description: 取得 active basic 裝置配對的轉譯器。
ms.assetid: DB2ED5D3-CCDF-4704-A29A-F1A13F7B953A
keywords:
- 轉譯器屬性媒體串流 API
- 轉譯器屬性媒體串流 API，DevicePair 介面
- DevicePair 介面媒體串流 API，轉譯器屬性
topic_type:
- apiref
api_name:
- DevicePair.Renderer
- DevicePair.get_Renderer
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f74b212ed4e8ec29b0234a3769c3beff91c0c777
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375064"
---
# <a name="devicepairrenderer-property"></a><span data-ttu-id="7faee-106">DevicePair：：轉譯器屬性</span><span class="sxs-lookup"><span data-stu-id="7faee-106">DevicePair::Renderer property</span></span>

<span data-ttu-id="7faee-107">取得 active basic 裝置配對的轉譯器。</span><span class="sxs-lookup"><span data-stu-id="7faee-107">Gets the renderer for the active basic device pair.</span></span>

<span data-ttu-id="7faee-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="7faee-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7faee-109">語法</span><span class="sxs-lookup"><span data-stu-id="7faee-109">Syntax</span></span>


```C++
HRESULT get_Renderer(
  [out] ActiveBasicDevice **value
);
```



## <a name="property-value"></a><span data-ttu-id="7faee-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="7faee-110">Property value</span></span>

<span data-ttu-id="7faee-111">接收代表轉譯器裝置的 [**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) 物件。</span><span class="sxs-lookup"><span data-stu-id="7faee-111">Receives a [**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)) object that represents the renderer device.</span></span>

## <a name="see-also"></a><span data-ttu-id="7faee-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7faee-112">See also</span></span>

<dl> <dt>

<span data-ttu-id="7faee-113">[**DevicePair**](/previous-versions/windows/desktop/legacy/dn385771(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7faee-113">[**DevicePair**](/previous-versions/windows/desktop/legacy/dn385771(v=vs.85))</span></span>
</dt> </dl>

 

 