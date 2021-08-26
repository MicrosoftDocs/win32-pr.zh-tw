---
description: 就像應用程式需要顯示裝置內容 (DC) ，才能開始在視窗的工作區中繪製，需要有印表機 DC 才能開始將輸出傳送至印表機。
ms.assetid: 5bdcec28-e28d-402d-8d80-e8aa5ecb4e74
title: '印表機裝置內容 (檔和列印) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c868d5bf8247375375b33bcb034a70bd6f28c5b9104b61e264543a63281069
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947398"
---
# <a name="printer-device-contexts-documents-and-printing"></a>印表機裝置內容 (檔和列印) 

就像應用程式需要顯示裝置內容 (DC) ，才能開始在視窗的工作區中繪製，需要有印表機 DC 才能開始將輸出傳送至印表機。 印表機 DC 與顯示 DC 類似，因為它是內部資料結構，它會定義一組繪圖物件和其相關聯的屬性，並指定影響輸出的圖形模式。 繪圖物件包括線條繪圖的畫筆、繪製和填滿的筆刷，以及文字輸出的字型。

與顯示 DC 不同的是，印表機 DC 並非由 window 管理元件所擁有，而且無法藉由呼叫 [**GetDC**](/windows/desktop/api/winuser/nf-winuser-getdc) 函式取得。 相反地，應用程式必須呼叫 [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) 或 [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85)) 函數。

如果您的應用程式呼叫 [**CreateDC**](/windows/desktop/api/wingdi/nf-wingdi-createdca) 函式，它必須提供驅動程式和埠名稱。 若要取得這些名稱，請呼叫 [**GetPrinter**](getprinter.md) 或 [**>enumprinters**](enumprinters.md) 函數。

如果您的應用程式呼叫 [**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85))函式，並 \_ 在 [**PrintDlgEx**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa)結構的 **旗標** 成員中指定 PD RETURNDC 值，系統會針對使用者選取的印表機傳回裝置內容控制碼。 如需詳細資訊，請參閱[使用通用對話方塊](../dlgbox/using-common-dialog-boxes.md)中的[列印屬性工作表](../dlgbox/print-property-sheet.md)和「使用列印屬性工作表」。

 

 
