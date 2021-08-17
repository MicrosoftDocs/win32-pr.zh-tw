---
description: SourceListForceResolution 方法會清除最後使用的來源屬性。
ms.assetid: 9ecfdf6e-4fed-46fc-8956-85d20cbe5327
title: SourceListForceResolution 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListForceResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a02e538a1d61fb0adf081542f10dea29f2a636e36b9ce936d7d282e30823339d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065858"
---
# <a name="patchsourcelistforceresolution-method"></a>SourceListForceResolution 方法

**SourceListForceResolution** 方法會清除最後使用的來源屬性。 這會強制安裝程式在下次需要 patch 來源時，于來源清單中搜尋有效的 patch 來源。 例如，安裝程式要求修補程式來源在修補程式的本機快取複本遺失時，執行安裝或重新安裝。 這個方法會呼叫 [**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)。

## <a name="syntax"></a>語法


```JScript
Patch.SourceListForceResolution()
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

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

[**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




