---
description: 在 TAPI 層級中，應用程式可以傳遞各種不同的參數，其中有許多可能無效。
ms.assetid: cc52e2a2-08e0-4a66-a75f-975e50dbf654
title: " (電話語音 API) 檢查時發生錯誤"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 072ee8e456ed255da6945adef7a0bba872870a8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976887"
---
# <a name="error-checking"></a>錯誤檢查

在 TAPI 層級中，應用程式可以傳遞各種不同的參數，其中有許多可能無效。 TAPI 會驗證參數，並將錯誤傳回給應用程式，而不需呼叫服務提供者。 TSPI 層級上的每個函數描述都會描述已測試過的參數錯誤。 服務提供者不需要重複這些測試，但它必須執行任何適用于此函數的其他有效性測試。 下表列出在許多函式中出現的一般參數有效性測試的標題和描述。



| 有效性測試       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 指標有效性    | TAPI 已測試資料儲存體的指標，以確保其指向適合作業的可讀取或可寫入記憶體大小。 此外，對於從 **dwTotalSize** 成員開始的大小可變大小資料結構，資料結構已經過驗證，以確保可使用指定的總大小。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| 固定大小有效性 | 針對變動大小的資料結構，資料結構已經過驗證，因此是資料結構固定大小部分的空間，而且該 **dwTotalSize** 對固定部分已足夠。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 位移/大小為零  | 若為變數大小的資料結構，則為 ".。。**Offset**"and" .。。[**大小**] 欄位，這些欄位對應至服務提供者所設定的元件，在呼叫服務提供者之前，已預先預設為零個值。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| 控制碼有效性     | TAPI 可確保 [HDRVLINE](hdrvline.md)、 [HDRVPHONE](hdrvphone.md)和 HDRVCALL) 所定義類型 (的線路、電話和呼叫控制碼都有效。 也就是說，它們是在 [**TSPI \_ lineOpen**](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)、 [**TSPI \_ phoneOpen**](/windows/win32/api/tspi/nf-tspi-tspi_phoneopen)或下列其中一項啟動呼叫控制碼存留期的情況下，傳回的值沒有錯誤： [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)<br/> [**TSPI \_ lineCompleteTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer)<br/> [**TSPI \_ lineForward**](/windows/win32/api/tspi/nf-tspi-tspi_lineforward)<br/> [**TSPI \_ linePickup**](/windows/win32/api/tspi/nf-tspi-tspi_linepickup)<br/> [**TSPI \_ linePrepareAddToConference**](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference)<br/> [**TSPI \_ lineSetupConference**](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference)<br/> [**TSPI \_ lineSetupTransfer**](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)<br/> [**TSPI \_ lineUnpark**](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark)<br/> [**行 \_NEWCALL**](line-newcall.md) 訊息<br/> |



 

 

