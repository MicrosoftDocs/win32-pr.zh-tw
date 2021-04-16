---
title: AccNavigate_ReturnedElementWithIncorrectParent
description: AccNavigate \_ ReturnedElementWithIncorrectParent
ms.assetid: 44447E47-04D5-4784-B5E9-E8C62A9834CE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3bdff54c9c594cde4e6e57fe1886a900c913eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104571300"
---
# <a name="accnavigate_returnedelementwithincorrectparent"></a>AccNavigate \_ ReturnedElementWithIncorrectParent

## <a name="text"></a>Text

呼叫 accNavigate ( (Live Search) ，0，NAVDIR \_ FIRSTCHILD) 傳回 (x-小工具：///gadget.html) 傳回不正確的父系 (\[ Null \]) ，而不是 (即時搜尋) 

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

在 [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (使用 NAVDIR FIRSTCHILD 或 NAVDIR LASTCHILD 導覽常數) 所傳回的子專案上呼叫 [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)時 \_ \_ ，傳回的父項目不符合 **accNavigate** 呼叫中指定的父元素。

![傳回不正確父項目的無效 msaa 實作為範例。](images/accchecker-invalid-msaa-parent.png)

此問題可能會導致自動化工具的導覽問題，因為進行中的元素可能不穩定且無法預測。

## <a name="possible-causes"></a>可能的原因

不正確或不正確 MSAA 執行。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IAccessible：： accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[**IAccessible：： get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




