---
title: ORPC_DBG_BUFFER 結構
description: ORPC \_ DBG \_ 緩衝區結構是用來將 RPC 資料封送處理至 IOrpcDebugNotify 介面之方法的緩衝區格式。
ms.assetid: 444cd3b8-bc7b-425d-9ccc-04fd6c7393b2
keywords:
- ORPC_DBG_BUFFER 結構 COM
- PORPC_DBG_BUFFER 結構指標 COM
topic_type:
- apiref
api_name:
- ORPC_DBG_BUFFER
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dc42251b928207a2b009a18c1d88e94dcf1492a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969764"
---
# <a name="orpc_dbg_buffer-structure"></a>ORPC \_ DBG \_ 緩衝區結構

**ORPC \_ DBG \_ 緩衝區** 結構是用來將 RPC 資料封送處理至 [**IOrpcDebugNotify**](iorpcdebugnotify.md)介面之方法的緩衝區格式。

## <a name="syntax"></a>語法


```C++
typedef struct _ORPC_DBG_BUFFER {
  DWORD alwaysOrSometimes;
  BYTE  verMajor;
  BYTE  verMinor;
  DWORD cbRemaining;
  GUID  guidSemantic;
  union {
    BOOL   fStopOnOtherSide;
    USHORT wDebuggingOpCode;
    USHORT cExtent;
    BYTE   padding[2];
    struct {
      ULONG cb;
      GUID  guidExtent;
      BYTE  *rgbData;
    };
  };
} ORPC_DBG_BUFFER, *PORPC_DBG_BUFFER;
```



## <a name="members"></a>成員

<dl> <dt>

**alwaysOrSometimes**
</dt> <dd>

控制偵錯工具產生的值。 **alwaysOrSometimes** 可以是下列其中一個值：



| 值                                                                                                                                                                                                                                                                   | 意義                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ORPC_DEBUG_ALWAYS"></span><span id="orpc_debug_always"></span><dl> <dt>**ORPC \_DEBUG \_ ALWAYS**</dt> <dt>0x00000000</dt> </dl>                              | 如果設定，COM 一律會在接收者上引發用戶端或伺服器通知。<br/>                                                                                                                                                    |
| <span id="ORPC_DEBUG_IF_HOOK_ENABLED"></span><span id="orpc_debug_if_hook_enabled"></span><dl> <dt>**ORPC \_\_如果 \_ \_ 已啟用**</dt>攔截，則進行調試 <dt></dt> </dl> | 如果設定，則只有在 **fTrace** 設為 **TRUE** 的情況下，藉由呼叫 DllDebugObjectRPCHook 中的 [](dlldebugobjectrpchook.md)來啟用 com 偵錯工具，com 才會在接收者上引發用戶端或伺服器通知。 <br/> |



 

</dd> <dt>

**>vermajor**
</dt> <dd>

資料格式規格的主要版本號碼。

</dd> <dt>

**>verminor**
</dt> <dd>

資料格式規格的次要版本號碼。

</dd> <dt>

**cbRemaining**
</dt> <dd>

在此結構中遵循的位元組數目（包含 **cbRemaining**）。

</dd> <dt>

**guidSemantic**
</dt> <dd>

GUID，可判斷下列等位的成員。 **guidSemantic** 可以採用下列其中一個值：



| 值                                                                                                           | 意義                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>9CADE560-8F43-101A-B07B-00DD01113F11</dt> </dl> | 判斷偵錯工具是否要執行單一逐步執行。 以下只會顯示聯集的 **fStopOnOtherSide** 成員。<br/>                                             |
| <dl> <dt>D62AEDFA-57EA-11ce-A964-00AA006C3706</dt> </dl> | 判斷是否要將 RPC 封送處理的資料和調試碼處理碼傳遞給接收者。 Union 的所有成員都存在於下方，但 **fStopOnOtherSide** 除外。<br/> |



 

</dd> <dt>

**fStopOnOtherSide**
</dt> <dd>

若 **為 TRUE**，則偵錯工具會執行單一逐步執行，並在到達另一端時，從伺服器跳過並繼續執行。 否則，不會執行單一逐步執行，而且偵錯工具會在另一端停止執行。

</dd> <dt>

**wDebuggingOpCode**
</dt> <dd>

值，允許指定一系列作業的其中一個。 **wDebuggingOpCode** 可以採用下列其中一個值：



| 值                                                                             | 意義                                                                                              |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x0000</dt> </dl> | 無作業。<br/>                                                                             |
| <dl> <dt>0x0001</dt> </dl> | 如果設定，則在設定為 **TRUE** 時，單一步驟的語義與 **fStopOnOtherSide** 相同。<br/> |



 

</dd> <dt>

**cExtent**
</dt> <dd>

填充。 請勿使用。

</dd> <dt>

**padding**
</dt> <dd>

填充。 請勿使用。

</dd> <dt>

**Cb**
</dt> <dd>

**RgbData** 中資料的大小（以位元組為單位）。

</dd> <dt>

**guidExtent**
</dt> <dd>

判斷 **rgbData** 中之資料類型的 **GUID** 。 **guidExtent** 可以採用下列其中一個值：



| 值                                                                                                           | 意義                                                   |
|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>53199051-57EB-11ce-A964-00AA006C3706</dt> </dl> | **rgbData** 是已封送處理的介面指標。<br/> |



 

</dd> <dt>

**rgbData**
</dt> <dd>

**位元組** 緩衝區，用來在用戶端與伺服器偵錯工具之間傳遞 RPC 封送處理的 COM 資料。 **RgbData** 的內容取決於 **GuidExtent** 中的 **GUID** 。



| guidExtent 值                     | rgbData 內容                                                                                                                                                                                                                                    |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 53199051-57EB-11ce-A964-00AA006C3706 | 呼叫 [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface)所產生的封送處理介面指標。 已封送處理的指標會使用 [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)轉換成其對應的介面指標。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

這個結構的成員具有1位元組的對齊方式，而且一律以位元組由小到大的順序傳輸。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                     |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>N/A</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ORPC \_ DBG \_ ALL**](orpc-dbg-all.md)
</dt> <dt>

[**ORPC \_ INIT 引數 \_**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

 





