---
description: 將 TRANSFORMSSECURE 屬性設定為1，會通知安裝程式在使用者電腦上的本機電腦上，將轉換快取到使用者沒有寫入存取權的位置。
ms.assetid: 414025c3-7b83-42c7-9954-7393fba06061
title: TRANSFORMSSECURE 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7af3432b8f895d4d9f5d0fe643ef8106e01e28ad64fb2db177e968fbc13d88de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141631"
---
# <a name="transformssecure-property"></a>TRANSFORMSSECURE 屬性

將 **TRANSFORMSSECURE** 屬性設定為1，會通知安裝程式在使用者電腦上的本機電腦上，將轉換快取到使用者沒有寫入存取權的位置。 設定此屬性就像是設定 [TransformsSecure 原則](transformssecure-policy.md) ，但範圍不同。 設定 TransformsSecure 原則會套用至指定使用者所安裝的所有套件。 無論使用者是哪一種，設定 **TRANSFORMSSECURE** 屬性都會套用至封裝。

這個屬性的目的是要提供安全轉換存放裝置給 Windows 2000 的旅遊使用者使用。 設定這個屬性時， [維護安裝](maintenance-installation.md) 只能從指定的路徑使用轉換。 如果路徑無法使用，維護安裝將會失敗。 因此，每個安全轉換的來源都必須位於安裝套件來源的位置。 然後，如果安裝程式發現本機電腦上缺少轉換，就可以從這個來源還原轉換。

## <a name="remarks"></a>備註

Windows安裝程式會將 [**TRANSFORMSATSOURCE**](transformsatsource.md)屬性解釋為與 **TRANSFORMSSECURE** 屬性相同。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[資料庫轉換](database-transforms.md)
</dt> </dl>

 

 




