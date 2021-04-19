---
description: IAMTimelineTransable 介面會將轉換新增至 DirectShow 編輯服務 (DES) 中的物件。
ms.assetid: 1be9adaa-4145-447c-b307-dabb4419c86c
title: 'IAMTimelineTransable 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d083b768e8dcf54236945755f4b26ecf13409b40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999518"
---
# <a name="iamtimelinetransable-interface"></a>IAMTimelineTransable 介面

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`IAMTimelineTransable`介面會將轉換新增至[DirectShow 編輯服務](directshow-editing-services.md) (DES) 中的物件。 這個介面是由任何可以套用轉換的物件所公開，包括追蹤、組合和群組。 執行這個介面的物件可以有任意數目的轉換，但轉換不能以時間重迭。

> [!Note]  
> 音訊不支援轉換。 音訊群組內的物件可以公開 `IAMTimelineTransable` 介面，但應用程式不應該將轉換新增至其中。

 

## <a name="members"></a>成員

**IAMTimelineTransable** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IAMTimelineTransable** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IAMTimelineTransable** 介面具有這些方法。



| 方法                                                          | 描述                                                                                                                        |
|:----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**GetNextTrans**](iamtimelinetransable-getnexttrans.md)       | 抓取在指定時間或之後出現的第一個轉換。<br/>                                             |
| [**GetNextTrans2**](iamtimelinetransable-getnexttrans2.md)     | 使用指定的時間做為 **REFTIME** 值，抓取在指定時間或之後出現的第一個轉換。<br/> |
| [**GetTransAtTime**](iamtimelinetransable-gettransattime.md)   | 抓取最接近指定時間的轉換。<br/>                                                                 |
| [**GetTransAtTime2**](iamtimelinetransable-gettransattime2.md) | 在指定為 **REFTIME** 值的情況下，抓取最接近指定時間的轉換。<br/>                                   |
| [**TransAdd**](iamtimelinetransable-transadd.md)               | 將轉換新增至物件。<br/>                                                                                        |
| [**TransGetCount**](iamtimelinetransable-transgetcount.md)     | 捕獲此物件的轉換數目。<br/>                                                                     |



 

## <a name="remarks"></a>備註

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



 

 
