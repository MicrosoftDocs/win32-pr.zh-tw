---
description: 抓取框架的目的位址。
ms.assetid: f19a6753-37d8-4ec7-a7d4-ced0292d453c
title: 'GetFrameDestAddress 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameDestAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: afec32f0e0fc66ccd5a1d78cc9769b0e742f1e6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936629"
---
# <a name="getframedestaddress-function"></a>GetFrameDestAddress 函式

**GetFrameDestAddress** 函式會捕獲框架的目的位址。

## <a name="syntax"></a>語法


```C++
DWORD WINAPI GetFrameDestAddress(
   HFRAME    hFrame,
   LPADDRESS lpAddress,
   DWORD     AddressType,
   DWORD     Flags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hFrame* 
</dt> <dd>

要取得指標之框架的控制碼。

</dd> <dt>

*lpAddress* 
</dt> <dd>

儲存框架目的地位址的傳回緩衝區。

</dd> <dt>

*AddressType* 
</dt> <dd>

網址類別型，例如位址 \_ 類型 \_ ETHERNET 或位址 \_ 類型 \_ IP。

</dd> <dt>

*旗標* 
</dt> <dd>

用來修改傳回之目的地位址資料的旗標。



| 值                                                                                                                                                                                                           | 意義                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="ADDRESSTYPE_FLAGS_NORMALIZE"></span><span id="addresstype_flags_normalize"></span><dl> <dt>**ADDRESSTYPE \_ 旗標正規化 \_**</dt> </dl>        | 取消路由和群組位。<br/>                   |
| <span id="ADDRESSTYPE_FLAGS_BIT_REVERSE"></span><span id="addresstype_flags_bit_reverse"></span><dl> <dt>**ADDRESSTYPE \_ 旗標 \_ 位 \_ 反轉**</dt> </dl> | 將權杖通道的網路位址轉譯回一般。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則 *lpAddress* 值有效，且傳回值為 BHERR \_ SUCCESS。

如果函式不成功，則傳回值為錯誤碼。



| 傳回碼                                                                                                | Description                                                                                |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ \_ 找不到 BHERR 通訊協定 \_**</dt> </dl> | *AddressType* 參數中指定的通訊協定對框架而言無效。<br/> |
| <dl> <dt>**BHERR \_ 不正確 \_ HFRAME**</dt> </dl>      | *HFrame* 值無效。<br/>                                                  |



 

## <a name="remarks"></a>備註

允許 **位址 \_ 類型 \_ 尋找 \_ 最高** 的網址類別型。 使用此網址類別型時，此函式會先搜尋 IPX、XNS、IP 或 VINES IP 位址，再傳回 ETHERNET、TOKENRING 或 FDDI 位址。 這種方法適用于通訊協定和環境，在此環境中，可在單一伺服器位址下多工處理兩個 Nic。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>  |
| 程式庫<br/>                  | <dl> <dt>Nmapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




