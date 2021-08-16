---
description: State 屬性會傳回這個 patch 實例的安裝狀態。
ms.assetid: b01b2839-d867-4353-99d0-8c612cd1eb0c
title: Patch。 State 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.State
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b28eee03cfc74537c8be7669124a4f70db40ca88196678889553978232c934c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942288"
---
# <a name="patchstate-property"></a>Patch。 State 屬性

**State** 屬性會傳回這個 patch 實例的安裝狀態。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Patch.State
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

這個屬性會傳回下列其中一個值。



| 安裝狀態        | 意義                                                      |
|---------------------------|--------------------------------------------------------------|
| 套用 \_ 的 MSIPATCHSTATE    | Patch 會套用至此產品實例。                   |
| MSIPATCHSTATE 已被 \_ 取代 | Patch 已套用至此產品實例，但已被取代。 |
| MSIPATCHSTATE 已 \_ 過時  | Patch 已套用於此產品實例，但已淘汰。      |



 

\_ \_ 如果 [**修補程式**](patch-object.md)物件是以空字串來初始化， 則這個方法可能會傳回錯誤未知的修補程式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003、Windows XP 和 Windows 2000 上的安裝程式3.0 或更新版本<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IPatch 定義為000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




