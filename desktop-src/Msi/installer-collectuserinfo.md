---
description: 安裝程式物件的 CollectUserInfo 方法會叫用使用者介面 wizard 順序，以收集並儲存使用者資訊和產品代碼。
ms.assetid: 2faacf38-1af1-4e8a-a3f6-87733104614e
title: CollectUserInfo 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CollectUserInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d7286fdbc9fab6b3db6752284bf86db05f920bd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982645"
---
# <a name="installercollectuserinfo-method"></a>CollectUserInfo 方法

[**安裝程式**](installer-object.md)物件的 **CollectUserInfo** 方法會叫用使用者介面 wizard 順序，以收集並儲存使用者資訊和產品代碼。

## <a name="syntax"></a>語法


```JScript
Installer.CollectUserInfo(
  Product
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*產品* 
</dt> <dd>

指定產品的 [**產品代碼**](productcode.md) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

應用程式在第一次執行時，應該呼叫 **CollectUserInfo** 方法。 **CollectUserInfo** 方法會開啟產品的安裝套件，並叫用可收集使用者資訊的撰寫使用者介面 wizard 順序。 完成嚮導順序時，會註冊所收集的使用者資訊。 [**UILevel**](installer-uilevel.md)屬性應該設定為 msiUILevelFull，因為此 API 需要撰寫的使用者介面。

**CollectUserInfo** 方法會叫用 [ [firstrun.cmd] 對話方塊](firstrun-dialog.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa)
</dt> </dl>

 

 




