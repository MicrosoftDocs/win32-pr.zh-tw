---
description: ComponentPath 屬性是唯讀屬性，會傳回已安裝元件的完整路徑。 如果元件的金鑰路徑是登錄機碼，則會傳回登錄機碼。
ms.assetid: 6e53419d-f28a-45cd-abc8-0f451177f3fc
title: ComponentPath 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentPath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e249290af2477d2dfcbc73f80f80b439f1dd3663
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989643"
---
# <a name="installercomponentpath-property"></a>ComponentPath 屬性

**ComponentPath** 屬性是唯讀屬性，會傳回已安裝元件的完整路徑。 如果元件的金鑰路徑是登錄機碼，則會傳回登錄機碼。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Installer.ComponentPath
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

如果元件是登錄機碼，則會以數位表示登錄根目錄。 例如，"HKEY \_ CURRENT \_ USER SOFTWARE microsoft" 的登錄路徑會 \\ \\ 以 "01： \\ SOFTWARE \\ microsoft" 傳回。 傳回的登錄根目錄定義如下：



| Root                    | 傳回值 |
|-------------------------|----------------|
| HKEY \_ 類別 \_ 根目錄     | 00             |
| HKEY \_ 目前的 \_ 使用者     | 01             |
| HKEY \_ 本機 \_ 電腦    | 02             |
| HKEY \_ 使用者             | 03             |
| HKEY \_ 效能 \_ 資料 | 04             |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)
</dt> </dl>

 

 




