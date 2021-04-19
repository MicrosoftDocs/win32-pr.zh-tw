---
description: 唯讀 FeatureState 屬性會傳回功能的已安裝狀態。
ms.assetid: a3d30296-191e-4446-b5b1-a92f8991926a
title: FeatureState 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cf6fe61899ea1daac37fd678e9f0e70dfcc3af69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000672"
---
# <a name="installerfeaturestate-property"></a>FeatureState 屬性

唯讀 **FeatureState** 屬性會傳回功能的已安裝狀態。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Installer.FeatureState
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

這個屬性會傳回下列其中一個值。



| 值                     | 描述                                      |
|---------------------------|--------------------------------------------------|
| msiInstallStateAbsent     | 未安裝此功能。                    |
| msiInstallStateAdvertised | 已公告此功能。                       |
| msiInstallStateLocal      | 這項功能會安裝在本機執行。         |
| msiInstallStateSource     | 這項功能已安裝成從來源執行。     |
| msiInstallStateInvalidArg | 傳遞給函數的參數無效。 |
| msiInstallStateUnknown    | 產品代碼或功能識別碼未知。       |
| msiInstallStateBadConfig  | 設定資料已損毀。               |



 

 

**FeatureState** 屬性不會驗證是否可存取此功能。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea)
</dt> </dl>

 

 




