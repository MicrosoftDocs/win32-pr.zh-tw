---
description: 設定 ARPNOMODIFY 屬性會在修改產品的主控台中停用 [新增或移除程式] 功能。
ms.assetid: dc804910-cf15-4f9e-863f-78dcac248717
title: ARPNOMODIFY 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ee118c8b0e9d3c1cebef5aeefbf9e97c4793623
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984061"
---
# <a name="arpnomodify-property"></a>ARPNOMODIFY 屬性

設定 **ARPNOMODIFY** 屬性會在修改產品的主控台中停用 [新增或移除程式] 功能。 針對 Windows 2000，這會在 **主控台** 的 [**新增或移除程式**] 中停用產品的 [**修改**] 按鈕。 在舊版作業系統上，按一下 [ **新增或移除程式** ] 按鈕會卸載產品，而不是輸入維護模式的 wizard。

如果已設定 **ARPNOMODIFY** 屬性， [RegisterProduct 動作](registerproduct-action.md) 會在登錄機碼下寫入 "NoModify" 值：

**HKLM** \\**軟體** \\**Microsoft** \\**Windows** \\**CurrentVersion** \\**卸載** \\ **{*產品金鑰*}**

如果已設定 **ARPNOMODIFY** 屬性，而且未設定 [**ARPNOREMOVE**](arpnoremove.md) 屬性，則 RegisterProduct 動作也會在此機碼下寫入 UninstallString 值。 UnistallString 值是用來移除產品的命令列，而不是重新設定產品。

## <a name="remarks"></a>備註

在 Windows 2000 上，這會在 **主控台** 的 [**新增或移除程式**] 中停用產品的 [**變更**] 按鈕。

這個屬性可以透過自訂轉換來設定，以防止使用者透過 [ **新增或移除程式**] 來變更系統管理員的自訂。 這個屬性只會影響 [ **新增或移除程式**]。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[自訂轉換範例](a-customization-transform-example.md)
</dt> </dl>

 

 




