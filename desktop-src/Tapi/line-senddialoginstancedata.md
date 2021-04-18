---
description: TSPI LINE \_ SENDDIALOGINSTANCEDATA 訊息會使 TAPI \_ 在與 htDlgInst 相關聯的 UI DLL 中呼叫 TUISPI providerGenericDialogData 函式，並將 lpParams 所指向的參數區塊傳遞給長度為 dwSize 的。
ms.assetid: d3c176ba-8b4b-4b7c-a603-130dfa761898
title: 'LINE_SENDDIALOGINSTANCEDATA 訊息 (Tspi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0af7ae5bfc942d4408ac5ce2438cd9a88c1f1f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976247"
---
# <a name="line_senddialoginstancedata-message"></a>行 \_ SENDDIALOGINSTANCEDATA 訊息

TSPI **LINE \_ SENDDIALOGINSTANCEDATA** 訊息會使 TAPI 在與 *HTDLGINST* 相關聯的 UI DLL 中呼叫 [**TUISPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata)函式，並 *將 lpParams 所* 指向的參數區塊傳遞給長度為 *dwSize* 的。


```C++
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*htDlgInst* 
</dt> <dd>

使用 [**行 \_ CREATEDIALOGINSTANCE**](line-createdialoginstance.md)建立對話方塊實例時，傳回給服務提供者的 HTAPIDIALOGINSTANCE。

</dd> <dt>

*lpParams* 
</dt> <dd>

傳遞給 UI DLL [**TUISPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) 函式之提供者特定參數區塊的指標，其大小是由 *dwSize* 所指定。 如果這個參數設定為 **Null**，這就是立即關閉對話方塊的要求，清除 (UI DLL 不應該在此清除) 期間叫用 [**TUISPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) 。

</dd> <dt>

*dwSize* 
</dt> <dd>

要傳達給 UI DLL 之參數區塊的大小（以位元組為單位）。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 2.0 或更新版本<br/>                                             |
| 標頭<br/>       | <dl> <dt>Tspi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TUISPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback)
</dt> <dt>

[**TUISPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata)
</dt> <dt>

[**行 \_ CREATEDIALOGINSTANCE**](line-createdialoginstance.md)
</dt> </dl>

 

