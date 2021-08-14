---
description: ComponentState 屬性是此產品之實例的元件安裝狀態。這個屬性會使用物件的 ProductCode、UserSid 和內容來呼叫 MsiQueryComponentState。
ms.assetid: 2939048a-42a5-4ffb-868c-251c0f15e5ed
title: ComponentState 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.ComponentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d2bc9c5c1f5325dc631f8866ba1a8c7d88ce18d624a2974974f4692bf4f7b067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118376777"
---
# <a name="productcomponentstate-method"></a>ComponentState 方法

**ComponentState** 屬性是此產品之實例的元件安裝狀態。

這個屬性會使用物件的 ProductCode、UserSid 和內容來呼叫 [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)。 元件識別碼 GUID 會以參數形式提供。

## <a name="syntax"></a>語法


```JScript
Product.ComponentState(
  ID
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*識別碼* 
</dt> <dd>

元件 [資料表](component-table.md)的 [元件 id] 資料行中所找到元件的元件程式碼 GUID。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果呼叫成功，屬性會將值包含為 **DWORD**。



| 狀態                | 意義                                            |
|----------------------|----------------------------------------------------|
| INSTALLSTATE \_ 本機  | 元件會安裝在本機。                |
| INSTALLSTATE \_ 來源 | 元件會安裝成從來源執行。 |



 

如果呼叫失敗，屬性會包含 [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)中的錯誤碼。



| 錯誤                     | 意義                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| \_拒絕存取 \_ 錯誤     | 呼叫進程必須具有系統管理許可權，才能取得目前使用者以外的使用者資訊。 |
| 錯誤的設定不 \_ 正確 \_ | 設定資料已損毀。                                                                                 |
| 錯誤 \_ 不正確 \_ 參數 | 傳遞給函數的參數無效。                                                                   |
| 錯誤 \_ 成功            | 函數已順利完成。                                                                               |
| 錯誤 \_ 不明的 \_ 元件 | 元件識別碼不會識別已知的元件。                                                              |
| 錯誤 \_ 未知的 \_ 產品   | 產品代碼未識別已知的產品。                                                                |
| 錯誤函式 \_ \_ 失敗   | 未預期的內部失敗。                                                                                    |



 

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

[**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)
</dt> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




