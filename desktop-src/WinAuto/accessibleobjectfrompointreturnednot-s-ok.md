---
title: AccessibleObjectFromPointReturnedNot_S_OK
description: AccessibleObjectFromPointReturnedNot \_ S \_ 沒問題
ms.assetid: F5DA071A-EBB8-454C-9BC0-BC798835B7D0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba0ceabd15e5a401bb67ac14af5a7fb83b96543b4b8046ceee2349d8d57b8de5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327684"
---
# <a name="accessibleobjectfrompointreturnednot_s_ok"></a>AccessibleObjectFromPointReturnedNot \_ S \_ 沒問題

## <a name="text"></a>Text

AccessibleObjectFromPoint ({0} ， {1}) 傳回 {2} 且預期的 S \_ 確定

## <a name="type"></a>類型

警告

## <a name="description"></a>描述

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) 未 \_ 如預期般針對指定的座標傳回 S OK。

## <a name="possible-causes"></a>可能的原因

-   驗證期間的使用者互動，例如將焦點移至非目標 HWND，並干擾驗證程式。
-   不正確或不正確 MSAA 執行。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[流覽點擊測試和螢幕位置](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




