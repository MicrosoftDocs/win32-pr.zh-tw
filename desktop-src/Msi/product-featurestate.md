---
description: FeatureState 屬性是此產品實例之功能的安裝狀態。這個屬性會使用物件的 ProductCode、UserSid 和內容來呼叫 MsiQueryFeatureStateEx。 功能識別碼會以參數形式提供。
ms.assetid: 6821be80-4065-465e-b4c9-4cf17856bc5f
title: FeatureState 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.FeatureState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 484b8f7f3094cf5bca2cb9d03941d68619995ba98de08e2845c3717439709e2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129048"
---
# <a name="productfeaturestate-method"></a>FeatureState 方法

**FeatureState** 屬性是此產品實例之功能的安裝狀態。

這個屬性會使用物件的 *ProductCode*、 *UserSid* 和 *內容* 來呼叫 [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)。 功能識別碼會以參數形式提供。

## <a name="syntax"></a>語法


```JScript
Product.FeatureState(
  FeatureId
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*FeatureId* 
</dt> <dd>

功能識別碼出現在 [功能資料表](feature-table.md)的功能資料行中。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果呼叫成功，屬性會將值包含為 **DWORD**。



| 狀態                    | 意義                                      |
|--------------------------|----------------------------------------------|
| INSTALLSTATE \_ 公告 | 這項功能已公告。                  |
| INSTALLSTATE \_ 本機      | 這項功能會安裝在本機。            |
| INSTALLSTATE \_ 來源     | 這項功能已安裝成從來源執行。 |



 

如果呼叫失敗，屬性會包含 [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)中的錯誤碼。



| 錯誤                     | 意義                                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| \_拒絕存取 \_ 錯誤     | 呼叫進程必須具有系統管理許可權，才能取得針對目前使用者以外的使用者所安裝之產品的資訊。 |
| 錯誤的設定不 \_ 正確 \_ | 設定資料已損毀。                                                                                                         |
| 錯誤 \_ 不正確 \_ 參數 | 傳遞給函數的參數無效。                                                                                           |
| 錯誤 \_ 成功            | 函數已順利完成。                                                                                                       |
| 錯誤 \_ 未知的 \_ 功能   | 功能識別碼不會識別已知的功能。                                                                                          |
| 錯誤 \_ 未知的 \_ 產品   | 產品代碼未識別已知的產品。                                                                                        |
| 錯誤函式 \_ \_ 失敗   | 未預期的內部失敗。                                                                                                            |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003、Windows XP 和 Windows 2000 上的安裝程式3.0 或更新版本<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct 定義為000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**產品**](product-object.md)
</dt> <dt>

[**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)
</dt> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




