---
description: 如果設定了 LIMITUI 屬性，則在安裝套件時所使用的使用者介面 (UI) 層級會限制為「基本」。
ms.assetid: 1a75e66b-958a-4fa8-b13c-ced976c9508e
title: LIMITUI 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 969b6e1c1de5a55581fa8d24f6d538c829e18fb48afb9bdc2fd04bae69c15162
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013136"
---
# <a name="limitui-property"></a>LIMITUI 屬性

如果設定了 **LIMITUI** 屬性，則在安裝套件時所使用的使用者介面 (UI) 層級會限制為「基本」。 如果封裝中沒有任何撰寫的 UI，但仍包含 [對話方塊資料表](dialog-table.md)之類的 ui 資料表，則此屬性是必要的。 如需 UI 層級的說明，請參閱 [ **MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

## <a name="remarks"></a>備註

包含 **LIMITUI** 屬性的安裝套件也必須包含 [**ARPNOMODIFY**](arpnomodify.md) 屬性。 當您嘗試設定產品時，使用者必須從 **主控台** 公用程式中的 [**新增或移除程式**] 取得正確的行為。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)
</dt> <dt>

[**ARPNOMODIFY**](arpnomodify.md)
</dt> </dl>

 

 




