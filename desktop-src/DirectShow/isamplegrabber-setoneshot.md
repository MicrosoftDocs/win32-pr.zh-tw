---
description: SetOneShot 方法會指定範例抓取篩選器是否會在篩選器收到範例後停止。
ms.assetid: 7e3a3e8c-1834-425b-9657-279ab4451a2b
title: 'ISampleGrabber：： SetOneShot 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.SetOneShot
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 72a6e0e1798bcb8e19807619e982f487b0f04e6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982595"
---
# <a name="isamplegrabbersetoneshot-method"></a>ISampleGrabber：： SetOneShot 方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

**SetOneShot** 方法會指定 [**範例**](sample-grabber-filter.md)抓取篩選器是否會在篩選器收到範例後停止。

## <a name="syntax"></a>語法


```C++
HRESULT SetOneShot(
   BOOL OneShot
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*OneShot* 
</dt> <dd>

布林值，這個值會指定在接收到範例之後，範例抓取篩選器是否會中止。



| 值                                                                                                                                    | 意義                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE * * * *</dt> </dl>    | 範例捕獲會在第一個範例之後停止。 <br/>                                                      |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE * * * *</dt> </dl> | 在第一個範例之後，範例抓取程式會繼續處理範例。 這是預設行為。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

使用這個方法可從資料流程取得單一範例，如下所示：

1.  使用值 **TRUE** 來呼叫 **SetOneShot** 。
2.  （選擇性）使用 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 介面搜尋資料流程中的位置。
3.  呼叫 [**IMediaControl：： run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) 以執行篩選圖形。
4.  呼叫 [**IMediaEvent：： WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) 以等候圖形停止。 或者，您也可以呼叫 [**IMediaEvent：： GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) 來取得圖形事件，直到您收到 [**EC \_ 完成**](ec-complete.md) 事件為止。

在範例捕獲程式停止之後，篩選圖形仍處於執行中狀態。 您可以搜尋或暫停圖形來取得另一個範例。

> [!Note]  
> 舊版檔指出篩選圖形會在收到範例後停止。 這是不正確的。 資料流程結束，但圖形仍處於執行中狀態。

 

此範例會藉由呼叫下游篩選器上的 [**IPin：： EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) ，並 \_ 從它的 [**IMemInputPin：： Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) 方法傳回 FALSE，來執行一次模式。

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

[使用範例捕獲](using-the-sample-grabber.md)
</dt> <dt>

[**ISampleGrabber 介面**](isamplegrabber.md)
</dt> </dl>

 

 




