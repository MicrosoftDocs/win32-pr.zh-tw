---
description: TSPI LINE \_ CREATEDIALOGINSTANCE 訊息會使 TAPI 在服務提供者與在 \_ 應用程式內容中執行的 TUISPI providerGenericDialog 函式實例之間建立關聯。
ms.assetid: 5a7e34bc-1dc3-40c4-b07e-de5b88cbcd75
title: 'LINE_CREATEDIALOGINSTANCE 訊息 (Tspi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e670a0dbcdde82721e5441b95983d5852e821cc981062947a0d6b76639ad762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873498"
---
# <a name="line_createdialoginstance-message"></a>行 \_ CREATEDIALOGINSTANCE 訊息

TSPI **LINE \_ CREATEDIALOGINSTANCE** 訊息會使 TAPI 在服務提供者和 [**TUISPI \_ providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog)函式的實例之間建立關聯，而該應用程式是在叫用非同步 TSPI 函式的應用程式內容中執行，而該應用程式是由 [**dwRequestID 所指向 TUISPICREATEDIALOGINSTANCEPARAMS 結構的**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) *lpTUISPICreateDialogInstanceParams* 參數所 *識別。*


```C++
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*hProvider* 
</dt> <dd>

提供給服務提供者的 ProviderHandle，做為 [**TSPI \_ providerEnumDevices**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices)的參數。

</dd> <dt>

*lpTUISPICreateDialogInstanceParams* 
</dt> <dd>

[**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)結構的指標。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tspi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TSPI \_ providerEnumDevices**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices)
</dt> <dt>

[**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)
</dt> </dl>

 

