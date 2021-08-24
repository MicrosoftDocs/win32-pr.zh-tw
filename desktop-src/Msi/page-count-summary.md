---
description: '[頁面計數摘要] 屬性包含安裝套件所需的最低安裝程式版本。'
ms.assetid: ee3aaeed-166c-4591-ae3e-642c1204a5ca
title: 頁面計數摘要屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 690f19db5b8b4dc4dff3c3eb30f616803754bfac199a3aa1e6656da0f1e3fa39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145411"
---
# <a name="page-count-summary-property"></a>頁面計數摘要屬性

[ **頁面計數摘要** ] 屬性包含安裝套件所需的最低安裝程式版本。 至少要有 Windows Installer 2.0，這個屬性必須設定為整數200。 至少要有 Windows Installer 3.0，這個屬性必須設定為整數300。 至少要有 Windows Installer 3.1，這個屬性必須設定為301。 至少要有 Windows Installer 4.5，這個屬性必須設定為405。 至少要有 Windows Installer 5.0，這個屬性必須設定為500。

若為[64 位 Windows Installer 套件](64-bit-windows-installer-packages.md)，這個屬性必須設定為整數200或更高的整數。 若為 Arm64 平臺上的64位 Windows Installer 套件，這個屬性必須設定為整數500或更高的整數。

若為轉換封裝，[ **頁面計數摘要** ] 屬性會包含處理轉換所需的最低安裝程式版本。 設定為兩個 **頁面計數摘要** 屬性值的最大值，這些值屬於用來產生轉換的資料庫。

針對 patch 封裝，[ **頁面計數摘要** ] 屬性會設定為 Null。

這是必要的摘要屬性。

這個屬性可用來撰寫只能由指定的最小或更新版本 Windows Installer 安裝的封裝。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[摘要屬性描述](summary-property-descriptions.md)
</dt> </dl>

 

 




