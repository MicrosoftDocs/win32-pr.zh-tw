---
description: GetGroupOutputPin 方法會抓取指定群組的輸出圖釘。
ms.assetid: be4e17b6-15bf-43b1-8d93-d52d08c8bce6
title: 'IRenderEngine：： GetGroupOutputPin 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetGroupOutputPin
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 21e603e15f598c6d493e179a147391cb941a6c7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990721"
---
# <a name="irenderenginegetgroupoutputpin-method"></a>IRenderEngine：： GetGroupOutputPin 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

方法會抓取 `GetGroupOutputPin` 指定群組的輸出圖釘。

## <a name="syntax"></a>語法


```C++
HRESULT GetGroupOutputPin(
        long Group,
  [out] IPin **ppRenderPin
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*群組* 
</dt> <dd>

以零為基底的索引，可指定群組。

</dd> <dt>

*ppRenderPin* \[擴展\]
</dt> <dd>

接收輸出釘選 [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) 介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。 可能的值如下：



| 傳回碼                                                                                                  | Description                                                                |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>                      | 群組沒有輸出圖釘。<br/>                              |
| <dl> <dt>**S \_ 確定**</dt> </dl>                         | 成功。<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                 | 無效引數。<br/>                                               |
| <dl> <dt>**E \_ 必須 \_ INIT 轉譯器 \_**</dt> </dl>       | 轉譯引擎無法初始化。<br/>                             |
| <dl> <dt>**E \_ 指標**</dt> </dl>                    | 指標無效。<br/>                                                |
| <dl> <dt>**E \_ 轉譯 \_ 引擎 \_ 已 \_ 中斷**</dt> </dl> | 因為未成功轉譯專案，所以操作失敗。<br/> |
| <dl> <dt>**E 未 \_ 預期**</dt> </dl>                 | 非預期的錯誤。<br/>                                               |



 

## <a name="remarks"></a>備註

在呼叫這個方法之前，請先呼叫 [**IRenderEngine：： ConnectFrontEnd**](irenderengine-connectfrontend.md) 來建立圖形的前端。 每個群組都代表一個媒體資料流程，而前端則有對應的輸出圖釘。

您可以使用這個方法來建立檔案寫入圖形的轉譯部分。 將輸出圖釘連接到多工器篩選器和檔案寫入器篩選器。 如需詳細資訊，請參閱 [呈現專案](rendering-a-project.md)。

若為預覽版本，您不需要呼叫此方法。 只要呼叫 **ConnectFrontEnd** ，然後再呼叫 [**IRenderEngine：： RenderOutputPins**](irenderengine-renderoutputpins.md)。

如果方法傳回 S \_ OK，則傳回的 **IPin** 介面具有未處理的參考計數。 使用完畢後，請務必釋放介面。

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

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

 

 




