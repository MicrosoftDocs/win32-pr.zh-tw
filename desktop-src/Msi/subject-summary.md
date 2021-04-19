---
description: '[主旨摘要] 屬性的值會傳達封裝所安裝之產品、轉換或修補程式的名稱。'
ms.assetid: fb08a240-db30-477f-8dc0-701156d73cfc
title: 主體摘要屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d21139f686bc8a6cfc5ba2edecdfc57c349d84ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993313"
---
# <a name="subject-summary-property"></a>主體摘要屬性

[主旨 **摘要** ] 屬性的值會傳達封裝所安裝之產品、轉換或修補程式的名稱。

它是由安裝資料庫、轉換或修補套件的作者所組成，以提供摘要資訊中這個屬性的值。 作者應該執行下列動作，以判斷正確的值。

-   將安裝套件中的 [主旨 **摘要** ] 屬性設定為與 [**ProductName**](productname.md) 屬性相同的值。
-   將轉換中的 [主旨 **摘要** ] 屬性設定為與原始安裝套件中的 [主旨 **摘要** ] 屬性相同的值。
-   在 patch 封裝的摘要資訊中，將 [主旨 **摘要** ] 屬性設定為包含產品名稱之修補程式的簡短描述。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md)
</dt> <dt>

[摘要屬性描述](summary-property-descriptions.md)
</dt> </dl>

 

 




