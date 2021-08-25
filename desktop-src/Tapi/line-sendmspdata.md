---
description: '\_當電話語音服務提供者 (TSP) 想要將資訊傳遞給媒體服務提供者 (MSP) 時，會傳送 TSPI LINE SENDMSPDATA 訊息。'
ms.assetid: 982f40b3-7758-493c-9d04-6480e3c9e86d
title: 'LINE_SENDMSPDATA 訊息 (Tspi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90a4f9086bb734f73a9a28817009c11d261442cf4253791b51e48e89d511b2ca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126208"
---
# <a name="line_sendmspdata-message"></a>行 \_ SENDMSPDATA 訊息

當電話語音服務提供者 (TSP) 想要將資訊傳遞給媒體服務提供者 (MSP) 時，會傳送 TSPI **LINE \_ SENDMSPDATA** 訊息。


```C++
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*htLine* 
</dt> <dd>

線路的 TAPI 控制碼。

</dd> <dt>

*htCall* 
</dt> <dd>

呼叫的 TAPI 控制碼。

</dd> <dt>

*dwMsg* 
</dt> <dd>

值行 \_ SENDMSPDATA。

</dd> <dt>

*dwParam1* 
</dt> <dd>

識別應該接收訊息的 MSP。 如果是0，則會將訊息傳送至所有 Msp。 這是傳遞給 [**TSPI \_ LineCreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance) 函數的控制碼。

</dd> <dt>

*dwParam2* 
</dt> <dd>

要傳遞至 MSP 的緩衝區。 TAPI 不會解讀緩衝區。

</dd> <dt>

*dwParam3* 
</dt> <dd>

*DwParam2* 中緩衝區的大小（以位元組為單位）。

</dd> </dl>

## <a name="remarks"></a>備註

服務提供者必須協調 TAPI 3.0 版或更新版本，此訊息才能運作。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2。2<br/>                                                      |
| 標頭<br/>       | <dl> <dt>Tspi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[關於媒體服務提供者 (MSP) ](./about-the-media-service-provider-msp-.md)
</dt> <dt>

[**TSPI \_ lineMSPIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
</dt> <dt>

[**TSPI \_ LineCreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
</dt> <dt>

[**TSPI \_ lineCloseMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
</dt> <dt>

[**TSPI \_ lineRecieveMSPData**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
</dt> <dt>

[**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps)
</dt> </dl>

 

