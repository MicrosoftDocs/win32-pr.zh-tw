---
description: ConnectFrontEnd 方法會從目前的時間軸建立篩選圖形的前端。
ms.assetid: ac484fd6-b88d-4c3a-bc4d-f118083d706d
title: 'IRenderEngine：： ConnectFrontEnd 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.ConnectFrontEnd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b7e0b00d467eb56dabaf6623f129ed1eb82945a1add63386b2b21fb01f725082
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154035"
---
# <a name="irenderengineconnectfrontend-method"></a>IRenderEngine：： ConnectFrontEnd 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`ConnectFrontEnd`方法會從目前的時間軸建立篩選圖形的前端。

## <a name="syntax"></a>語法


```C++
HRESULT ConnectFrontEnd();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的傳回值包括下列各項：



| 傳回碼                                                                                                  | 描述                                                                    |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                         | 成功。<br/>                                                            |
| <dl> <dt>**S \_ 警告 \_ OUTPUTRESET**</dt> </dl>          | 已刪除圖形的轉譯部分。<br/>                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                 | 未設定此轉譯引擎的時間軸。<br/>                             |
| <dl> <dt>**E \_ 必須 \_ INIT 轉譯器 \_**</dt> </dl>       | 轉譯引擎無法初始化。<br/>                                 |
| <dl> <dt>**E \_ 轉譯 \_ 引擎 \_ 已 \_ 中斷**</dt> </dl> | 因為未成功轉譯專案，所以作業失敗。<br/> |
| <dl> <dt>**E 未 \_ 預期**</dt> </dl>                 | 非預期的錯誤。<br/>                                                   |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl>      | 媒體類型無效。<br/>                                                 |



 

## <a name="remarks"></a>備註

這個方法不會建立篩選圖形的呈現部分。 應用程式必須將前端的輸出圖釘連接到所需的轉譯篩選器：

-   若要預覽，請呼叫 [**IRenderEngine：： RenderOutputPins**](irenderengine-renderoutputpins.md) 方法。
-   若要輸出檔案，請呼叫 [**IRenderEngine：： GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) 來取得每個群組的輸出針腳，然後將這些釘選到多工器篩選器。

如果您使用的是基本轉譯引擎，前端的輸出圖釘會產生未壓縮的資料。 如果您使用智慧型轉譯引擎，輸出圖釘會產生壓縮的資料。

如果您在建立篩選圖形之後變更時間軸，則必須再次呼叫 `ConnectFrontEnd` 以重建前端。 方法會盡可能保留圖形的呈現部分。 但是，如果您新增或刪除群組，或是變更群組的順序，就 `ConnectFrontEnd` 會刪除轉譯部分，而您的應用程式必須重建。 如果方法刪除了轉譯部分，則會傳回 S \_ 警告 \_ OUTPUTRESET。

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載[Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IRenderEngine 介面**](irenderengine.md)
</dt> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> </dl>

 

 




