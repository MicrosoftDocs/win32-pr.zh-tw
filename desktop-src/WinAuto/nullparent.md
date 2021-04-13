---
title: NullParent
description: NullParent
ms.assetid: F9563D73-66EF-4C66-8783-B034AA7A212E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 765217f8d2d46645358d590c5a93310b04da01b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300707"
---
# <a name="nullparent"></a>NullParent

## <a name="text"></a>Text

元素父系為 Null

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

在元素上呼叫 [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) 時，會傳回 Null。 **Get \_ accParent** 方法只有在驗證目標的根項目上呼叫時，才應該傳回 Null。

此問題可能會導致自動化工具的導覽問題，因為進行中的元素可能不穩定且無法預測。

## <a name="possible-causes"></a>可能的原因

不正確或不正確 MSAA 執行。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IAccessible：： accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[**IAccessible：： get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




