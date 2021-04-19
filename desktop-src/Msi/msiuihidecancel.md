---
description: 這個 Windows Installer 屬性工作表示內部使用者介面層級已設定為隱藏 [取消] 按鈕。
ms.assetid: 0e842bee-32c2-41ae-97f3-bc8b34960a44
title: MsiUIHideCancel 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a25a940921dd4b0d91155765ee6768ec0d6d2bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001922"
---
# <a name="msiuihidecancel-property"></a>MsiUIHideCancel 屬性

當內部使用者介面層級已設定為包含 \_ 具有 [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)函數的 INSTALLUILEVEL HIDECANCEL 或 [**安裝程式**](installer-object.md)物件的 [UILevel](installer-uilevel.md)屬性，或使用 [命令列選項](command-line-options.md)時，安裝程式會將 MsiUIHideCancel 屬性設定為1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer 3.0 或更新版本。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




