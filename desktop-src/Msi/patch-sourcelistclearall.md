---
description: Patch 物件的 SourceListClearAll 方法會清除所指定類型之所有來源的完整來源清單，以取得修補程式。 接受型別做為參數。 這個方法會呼叫 MsiSourceListClearAllEx。
ms.assetid: 9458a3db-8eaa-4067-875f-8fac68bdf1f8
title: SourceListClearAll 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearAll
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ae7de8c0a830000b3100e84cacbf088fefb592ddaa912a7737a35ea009a3cfe1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942298"
---
# <a name="patchsourcelistclearall-method"></a>SourceListClearAll 方法

[**Patch**](patch-object.md)物件的 **SourceListClearAll** 方法會清除所指定類型之所有來源的完整來源清單，以取得修補程式。 接受 *型* 別做為參數。 這個方法會呼叫 [**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)。

## <a name="syntax"></a>語法


```JScript
Patch.SourceListClearAll(
  Type
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*類型* 
</dt> <dd>

來源類型的類型（例如網路、URL 或媒體）。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

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

[**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)
</dt> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




