---
description: Put \_ size 方法會設定輸出大小和延展模式。
ms.assetid: 1186eee4-b5c1-4216-abb3-86ea03b2da40
title: 'IResize：:p ut_Size 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.put_Size
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 579cee086798e64abd07b25cc4f7bb14405157dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000763"
---
# <a name="iresizeput_size-method"></a>IResize：:p 的內容 \_ 大小方法

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`put_Size`方法會設定輸出大小和延展模式。

## <a name="syntax"></a>語法


```C++
HRESULT put_Size(
  [in] int Height,
  [in] int Width,
  [in] int Flags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*高度* \[在\]
</dt> <dd>

影片高度（以圖元為單位）。

</dd> <dt>

*寬度* \[在\]
</dt> <dd>

影片寬度（以圖元為單位）。

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

延展模式。 請參閱重 [**設大小旗標**](resize-flags.md) 的可能值。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

DES 可能會在呼叫 **put \_ 媒體** 之前或之後呼叫這個方法。 如果 DES 在呼叫 **put \_ 媒體** 之前呼叫這個方法，則篩選應選取位深度的預設值，並使用大小值來建立輸出媒體類型。 如果 DES 在呼叫 **put \_ 媒體** 之後呼叫這個方法，則篩選器應該使用新的大小來修改其目前的輸出類型。

DES 也可以在輸出連接之後，呼叫這個方法。 在這種情況下，請修改輸出類型，然後以新的類型重新連接輸出的 pin。 如需詳細資訊，請參閱重新 [連接 pin](reconnecting-pins.md) 。

*Flags* 參數會指定篩選應如何執行調整大小作業。

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 版本<br/> | DirectX 9.0 或更新版本<br/>                                                         |
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[錯誤和成功碼](error-and-success-codes.md)
</dt> <dt>

[**IResize 介面**](iresize.md)
</dt> </dl>

 

 




