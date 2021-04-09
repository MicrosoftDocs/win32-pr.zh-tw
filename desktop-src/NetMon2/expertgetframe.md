---
description: 從載入的捕獲傳回要求的框架。
ms.assetid: efd1cff5-a3a1-4910-b003-25b6e10dad6e
title: 'ExpertGetFrame 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertGetFrame
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2bd02bde8caf157b6df6b1dd772a8f7574df0e57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847742"
---
# <a name="expertgetframe-function"></a>ExpertGetFrame 函式

**ExpertGetFrame** 函式會從載入的捕獲傳回要求的框架。

## <a name="syntax"></a>語法


```C++
DWORD WINAPI ExpertGetFrame(
  _In_  HEXPERTKEY              hExpertKey,
  _In_  DWORD                   Direction,
  _In_  DWORD                   RequestFlags,
  _In_  DWORD                   RequestedFrameNumber,
  _In_  HFILTER                 hFilter,
  _Out_ LPEXPERTFRAMEDESCRIPTOR pEFrameDescriptor
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hExpertKey* \[在\]
</dt> <dd>

唯一的專家識別碼。 網路監視器在呼叫 [**Run**](run.md)函式時，將 *hExpertKey* 識別碼傳遞給專家。

</dd> <dt>

*方向* \[在\]
</dt> <dd>

識別網路監視器如何搜尋框架的值。



| 值                                                                                                                                                                                         | 意義                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="GET_SPECIFIED_FRAME"></span><span id="get_specified_frame"></span><dl> <dt>**取得 \_ 指定的 \_ 框架**</dt> </dl>              | 傳回要求的框架。<br/> |
| <span id="GET_FRAME_NEXT_FORWARD"></span><span id="get_frame_next_forward"></span><dl> <dt>**取得 \_ \_ 下一個畫面格 \_**</dt> </dl>    | 傳回下一個畫面格。<br/>      |
| <span id="GET_FRAME_NEXT_BACKWARD"></span><span id="get_frame_next_backward"></span><dl> <dt>**取得 \_ \_ 下一個畫面格 \_**</dt> </dl> | 傳回上一個畫面格。<br/>  |



 

</dd> <dt>

*RequestFlags* \[在\]
</dt> <dd>

旗標，指定網路監視器應該如何處理要求。 指定下列一或多個旗標。



| 值                                                                                                                                                                                             | 意義                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLAGS_DEFER_TO_UI_FILTER"></span><span id="flags_defer_to_ui_filter"></span><dl> <dt>**旗標 \_ 延後 \_ 至 \_ UI \_ 篩選**</dt> </dl> | 套用在 *hFilter* 中指定之專家的顯示篩選參數之前，請套用網路監視器在專家啟動時所使用的顯示篩選。<br/>                                                                                                                              |
| <span id="FLAGS_ATTACH_PROPERTIES"></span><span id="flags_attach_properties"></span><dl> <dt>**旗標 \_ 附加 \_ 屬性**</dt> </dl>      | 所有通訊協定剖析器在此畫面格所宣告的區段中找到的屬性會附加至框架。 如果未設定旗標， **pEFrameDescriptor**) 所傳回之 [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md)結構 (的 **lpPropertyTable** 欄位將會設定為 **Null**。<br/> |



 

</dd> <dt>

*RequestedFrameNumber* \[在\]
</dt> <dd>

要求的框架數目。

</dd> <dt>

*hFilter* \[在\]
</dt> <dd>

專家顯示篩選的控點。 如果專家沒有顯示篩選器，請將參數設定為 **Null**。

</dd> <dt>

*pEFrameDescriptor* \[擴展\]
</dt> <dd>

傳回的 [**EXPERTFRAMEDESCRIPTOR**](expertframedescriptor.md) 結構，它會描述框架。 專家必須配置和釋放此結構所使用的記憶體。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 NMERR \_ SUCCESS。

如果函式不成功，則傳回值會指出失敗的原因。 如果傳回值是 NMERR \_ 專家 \_ 終止，則專家必須立即清除並返回; 使用者已中止專家執行。

## <a name="remarks"></a>備註

如果您設定 FLAGS \_ 附加 \_ 屬性，呼叫所需的資源會比未設定旗標的資源還多。 如果未設定旗標，指標會指向原始框架和框架的相關資料。 如果設定此旗標，網路監視器會呼叫宣告框架一部分的每個剖析器，以將所有屬性附加至框架。 這可能是緩慢的進程。

\_ \_ 除非專家需要剖析器附加至框架的屬性，否則專家不應設定 FLAGS 附加屬性旗標。 如果可能，專家應該在沒有旗標的情況下呼叫 **ExpertGetFrame** 函式，然後直接從框架中解壓縮所需的資料。

如果專家呼叫 **ExpertGetFrame** 時沒有旗標 \_ 附加 \_ 屬性旗標，且需要與該框架相關聯的屬性 (事件，例如) ，專家會使用相同的參數來呼叫 **ExpertGetFrame** ，但下列專案除外：

``` syntax
Direction = EXPERT_GET_SPECIFIED_FRAME;
RequestFlags &= (~EXPERT_DEFER_TO_UI_FILTER) | EXPERT_ATTACH_PROPERTIES;
RequestedFrameNumber= (The actual frame number you want);
hFilter = NULL;
pEFrameDescriptor = (The same one as last time);
```

使用上述程式碼可確保專家取得所需的框架，而不需要再次呼叫篩選器程式碼。

您可以將 *hFilter* 參數設定為 **LPVOID**。 如果存在，則傳回的框架會傳遞此篩選器。 如果專家沒有可傳遞至函式的顯示篩選 (如果 *hFilter* 為 **Null** ) ，則不會篩選傳回的畫面格。

**ExpertGetFrame** 函式只能由執行 [**執行**](run.md)或 [**設定**](configure.md)匯出函數的專家呼叫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




