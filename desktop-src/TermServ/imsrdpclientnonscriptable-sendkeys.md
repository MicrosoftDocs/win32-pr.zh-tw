---
title: IMsRdpClientNonScriptable SendKeys 方法
description: 將一連串的按鍵傳送到控制項。 按鍵是掃描程式碼形式，也就是實際實體索引鍵的鍵盤資料。
ms.assetid: 1f07a9cc-4795-43cb-ac99-4bb70b8b544a
ms.tgt_platform: multiple
keywords:
- SendKeys 方法遠端桌面服務
- SendKeys 方法遠端桌面服務，IMsRdpClientNonScriptable 介面
- IMsRdpClientNonScriptable 介面遠端桌面服務，SendKeys 方法
- SendKeys 方法遠端桌面服務，IMsRdpClientNonScriptable2 介面
- IMsRdpClientNonScriptable2 介面遠端桌面服務，SendKeys 方法
- SendKeys 方法遠端桌面服務，IMsRdpClientNonScriptable3 介面
- IMsRdpClientNonScriptable3 介面遠端桌面服務，SendKeys 方法
- SendKeys 方法遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，SendKeys 方法
- SendKeys 方法遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，SendKeys 方法
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable.SendKeys
- IMsRdpClientNonScriptable2.SendKeys
- IMsRdpClientNonScriptable3.SendKeys
- IMsRdpClientNonScriptable4.SendKeys
- IMsRdpClientNonScriptable5.SendKeys
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9effa3bbd40eb64df55914b9adbc07a03ea0c465
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466008"
---
# <a name="imsrdpclientnonscriptablesendkeys-method"></a>IMsRdpClientNonScriptable：： SendKeys 方法

將一連串的按鍵傳送到控制項。 按鍵是掃描程式碼形式，也就是實際實體索引鍵的鍵盤資料。

## <a name="syntax"></a>語法


```C++
HRESULT SendKeys(
  [in] LONG         numKeys,
  [in] VARIANT_BOOL *pbArrayKeyUp,
  [in] LONG         *plKeyData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*numKeys* \[在\]
</dt> <dd>

要傳送的按鍵數目。 可以在一個作業中傳送的最大索引鍵數目是20。 如果此參數大於20，則方法會傳回 **E \_ INVALIDARG** 。 如需詳細資訊，請參閱接下來的＜備註＞一節。

</dd> <dt>

*pbArrayKeyUp* \[在\]
</dt> <dd>

大小等於 *numKeys* 的陣列。 如果對應的索引鍵為 UP，元素就是 **TRUE** ，如果對應的索引鍵已關閉，則為 **FALSE** 。

</dd> <dt>

*plKeyData* \[在\]
</dt> <dd>

大小等於 *numKeys* 的陣列。 陣列包含擊鍵資料，並且對應至 [WM \_ KEYDOWN](../inputdev/wm-keydown.md)訊息的 *lParam* 參數值。 資料會指定重複計數、掃描程式碼、擴充按鍵旗標、內容程式碼、先前的索引鍵狀態旗標，以及轉換狀態旗標。 如需此陣列中位的描述，請參閱 [WM \_ KEYDOWN](../inputdev/wm-keydown.md)。

*PbArrayKeyUp* 中的對應元素會指出金鑰是否為向上或向下。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 **S \_ OK** 。

## <a name="remarks"></a>備註

**SendKeys** 方法不會混合由本機使用者進行的按鍵，以及方法所傳送的按鍵。 傳遞至方法的所有按鍵都會以單一不可部分完成的順序傳送至遠端會話。

如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                     |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                               |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>       |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable 定義為2f079c4c-87b2-4afd-97ab-20cdb43038ae<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[WM \_ KEYDOWN](../inputdev/wm-keydown.md)
</dt> </dl>

 

