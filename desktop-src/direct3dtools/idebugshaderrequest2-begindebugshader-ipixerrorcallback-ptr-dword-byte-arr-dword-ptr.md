---
description: 要求開始對指定的資訊清單進行偵錯工具。
MS-HAID: vspixengine.IDebugShaderRequest2\_BeginDebugShader\_IPixErrorCallback\_ptr\_DWORD\_BYTE\_arr\_DWORD\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IDebugShaderRequest2：： BeginDebugShader 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B454D673-C14F-4A8F-9DA7-2C47510BE5DA
api_name:
- IDebugShaderRequest2.BeginDebugShader
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3f59ef2da1fff99ca7ceee28a8c69554eb76047e
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2021
ms.locfileid: "122632096"
---
# <a name="span-idvspixengineidebugshaderrequest2_begindebugshader_ipixerrorcallback_ptr_dword_byte_arr_dword_ptrspanidebugshaderrequest2begindebugshader-method"></a><span id="vspixengine.idebugshaderrequest2_begindebugshader_ipixerrorcallback_ptr_dword_byte_arr_dword_ptr"></span>IDebugShaderRequest2：： BeginDebugShader 方法

要求開始對指定的資訊清單進行偵錯工具。

## <a name="syntax"></a>語法


```C++
HRESULT BeginDebugShader(
   IPixErrorCallback * errorCallback,
   DWORD               instructionStreamSize,
   BYTE []             count1_instructionStream,
   DWORD *             pDevice
);
```

## <a name="parameters"></a>參數

*errorCallback*   
偵錯工具期間可能發生的錯誤回呼位址。

*instructionStreamSize*   
指令資料流程中的指令數目。

*count1 \_ instructionStream*   
指定的指令資料流程。

*pDevice*   
要傳遞至偵測引擎以便與此 (的偵測引擎進行通訊的位址) 的 readprocessmemory debug engine。

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>另請參閱

[**IDebugShaderRequest2**](/windows/desktop/direct3dtools/idebugshaderrequest2)

 

 
