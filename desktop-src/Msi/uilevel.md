---
description: 安裝程式會將 UILevel 屬性設定為使用者介面的層級。
ms.assetid: 9fc58026-f140-4218-b44f-50fc6b0ef3e9
title: UILevel 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83b48ebaeb246f42e552b93c974db92c78e54dbc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000800"
---
# <a name="uilevel-property"></a>UILevel 屬性

安裝程式會將 **UILevel** 屬性設定為使用者介面的層級。 內部 UI 是透過 [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)來啟用和設定。 這個屬性會設定為下列其中一種 INSTALLUILEVEL 資料類型。



| INSTALLUILEVEL          | 數值 | 使用者介面層級                        |
|-------------------------|---------------|---------------------------------------------|
| INSTALLUILEVEL \_ 無    | 2             | 完全無訊息安裝。             |
| INSTALLUILEVEL \_ 基本   | 3             | 簡單的進度和錯誤處理。         |
| INSTALLUILEVEL \_ 縮減 | 4             | 撰寫的 UI、已隱藏的 wizard 對話方塊。     |
| INSTALLUILEVEL \_ FULL    | 5             | 使用 [嚮導]、[進度]、[錯誤] 撰寫的 UI。 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[消費者介面](user-interface.md)
</dt> <dt>

[從自訂動作判斷 UI 層級](determining-ui-level-from-a-custom-action.md)
</dt> </dl>

 

 




