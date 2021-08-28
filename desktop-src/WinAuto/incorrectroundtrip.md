---
title: IncorrectRoundTrip
description: IncorrectRoundTrip
ms.assetid: 244537EB-E7DC-49E4-BEAF-CFE3ED25E0B2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a17f0ca96496a9e98c1068354e3a9efda27ca8cb0993f6f924ea68ef7d0c1436
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644731"
---
# <a name="incorrectroundtrip"></a>IncorrectRoundTrip

## <a name="text"></a>Text

呼叫 accNavigate ( (按一下 [延遲]，以在下列內容中再次提醒： ) 、1、NAVDIR \_ 下一) ，然後 accNavigate ( (開啟) ，2，NAVDIR 上一個) ，則應該會傳回 click 延遲，以便在下列情況下提醒： \_ (ChildId = 1) 

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

當往返方向反轉時，使用 [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) 來跨越驗證目標的專案樹狀結構並不會傳回相同的起始元素。

![導致不正確的往返流覽的無效 msaa 執行範例](images/accchecker-invalid-round-trip.png)

此問題可能會導致自動化工具的導覽問題，因為進行中的元素可能不穩定且無法預測。

## <a name="possible-causes"></a>可能的原因

不正確或不正確 MSAA 執行。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IAccessible：： accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> </dl>

 

 




