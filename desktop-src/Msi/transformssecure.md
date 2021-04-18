---
description: 將 TRANSFORMSSECURE 屬性設定為1，會通知安裝程式在使用者電腦上的本機電腦上，將轉換快取到使用者沒有寫入存取權的位置。
ms.assetid: 414025c3-7b83-42c7-9954-7393fba06061
title: TRANSFORMSSECURE 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5b7a30ab5e94fb646e2e8960b60fd97dc35557c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976253"
---
# <a name="transformssecure-property"></a>TRANSFORMSSECURE 屬性

將 **TRANSFORMSSECURE** 屬性設定為1，會通知安裝程式在使用者電腦上的本機電腦上，將轉換快取到使用者沒有寫入存取權的位置。 設定此屬性就像是設定 [TransformsSecure 原則](transformssecure-policy.md) ，但範圍不同。 設定 TransformsSecure 原則會套用至指定使用者所安裝的所有套件。 無論使用者是哪一種，設定 **TRANSFORMSSECURE** 屬性都會套用至封裝。

這個屬性的目的是要為安全轉換儲存提供 Windows 2000 的旅遊使用者。 設定這個屬性時， [維護安裝](maintenance-installation.md) 只能從指定的路徑使用轉換。 如果路徑無法使用，維護安裝將會失敗。 因此，每個安全轉換的來源都必須位於安裝套件來源的位置。 然後，如果安裝程式發現本機電腦上缺少轉換，就可以從這個來源還原轉換。

## <a name="remarks"></a>備註

Windows Installer 會將 [**TRANSFORMSATSOURCE**](transformsatsource.md) 屬性解釋為與 **TRANSFORMSSECURE** 屬性相同。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[資料庫轉換](database-transforms.md)
</dt> </dl>

 

 




