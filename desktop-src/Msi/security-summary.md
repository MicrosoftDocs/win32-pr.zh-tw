---
description: '[安全性摘要] 屬性會傳達封裝是否應該以唯讀方式開啟。'
ms.assetid: f064b899-8123-49e1-b275-511186f49750
title: 安全性摘要屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997f75e388d504afd1d62f1ae2813943807910d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978465"
---
# <a name="security-summary-property"></a>安全性摘要屬性

[ **安全性摘要** ] 屬性會傳達封裝是否應該以唯讀方式開啟。 資料庫編輯工具不應該修改唯讀的強制資料庫，而且應該在嘗試修改唯讀建議的資料庫時發出警告。 這個屬性的下列值適用于 Windows Installer 檔案。



| 值 | 描述           |
|-------|-----------------------|
| 0     | 沒有限制        |
| 2     | 建議使用唯讀 |
| 4     | 強制唯讀    |



 

這個屬性應該設定為唯讀建議的 (2) 安裝資料庫，以及對轉換或修補程式的唯讀強制 (4) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[摘要屬性描述](summary-property-descriptions.md)
</dt> </dl>

 

 




