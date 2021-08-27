---
description: 本節說明如何從原生 Windows 程式進行列印。
ms.assetid: D0AE8FF8-D02D-43D3-80CA-E13EAA894F87
title: 如何：從 Windows 程式列印
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2999f112285dfff389583b15f7c7c2913a3e125bc58713e2ba5f18973aa6e1ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971337"
---
# <a name="how-to-print-from-a-windows-program"></a>如何：從 Windows 程式列印

本節說明如何從原生 Windows 程式進行列印。

## <a name="overview"></a>概觀

列印通常是原生 Windows 程式不可或缺的一部分。 因此，它不是您在撰寫程式之後可以輕鬆新增的功能。 話雖如此，如果程式設計為使用 XPS 檔，則不需要太多額外的程式碼，就能轉譯檔內容以進行列印。 應用程式的 XPS 檔可以直接傳送到具有 XPSDrv 印表機驅動程式的印表機。

使用 [Xps 檔 api](/previous-versions/windows/desktop/dd316976(v=vs.85)) 來建立檔內容和 [xps 列印 api](xps-printing.md) ，以將檔內容傳送至印表機。 XPS 列印 API 會處理目的地印表機的檔內容。 如果選取的印表機具有 XPSDrv 印表機驅動程式，則會將檔傳送至印表機，而不需要任何額外的轉換。 如果選取的印表機有以 GDI 為基礎的印表機驅動程式，則程式也可以將內容傳送至印表機，而且 XPS 列印 API 會轉換檔內容，使其與以 GDI 為基礎的印表機驅動程式相容。 無論是哪一種情況，應用程式執行的處理方式都相同。

## <a name="printing-tasks"></a>列印工作

下列主題描述列印程式內容的基本步驟。

1.  **收集使用者的列印工作資訊。**

    一般情況下，當使用者從功能表中選取 [列印] 選項，而且程式顯示 [列印] 對話方塊來收集列印工作的詳細資料時，使用者就會起始列印工作。 使用者通常會選取印表機、複本數目，以及印表機設定詳細資料，例如雙面列印和裝訂。

    如需有關如何執行此動作的詳細資訊，請參閱 [如何：收集使用者的列印工作資訊](preparing-to-print.md)。

2.  **建立進度指標。**

    進度指示器可為使用者提供列印工作進度的意見反應。 進度列指示器可以是包含作業之 [ **取消** ] 按鈕的對話方塊一部分的進度列，也可以是主視窗底部狀態列中的進度列。

    如需進度指示器運作的詳細資訊，請參閱 [如何：顯示列印工作進度](cancel-dialog-box.md)。

    如需有關如何顯示列印工作進度的詳細資訊，請參閱[Windows 應用程式 UI 開發](/windows/desktop/windows-application-ui-development)指導方針中的資訊。

3.  **啟動列印執行緒。**

    在程式收集使用者的列印工作資訊之後，就可以啟動列印執行緒來執行檔的實際處理，以進行列印。

    如需列印執行緒的詳細資訊，請參閱 [如何：啟動和停止列印執行緒](how-to--start-and-stop-a-printing-thread.md)。

4.  **轉譯列印工作資料。**

    列印執行緒會轉譯檔資料以進行列印。 您應該將此處理細分為離散的處理步驟，讓使用者可以中斷處理並取消作業，以及不允許處理執行緒封鎖其他執行緒和進程。

    如需如何呈現列印工作資料的詳細資訊，請參閱 [如何：轉譯列印工作資料](how-to--render-the-print-job-data.md)。

5.  **監視列印工作進度。**

    執行每個處理步驟時，請更新進度列以通知使用。 計算完成所要求作業的處理步驟，然後在執行這些步驟時更新進度列。

6.  **關閉列印工作，並結束列印執行緒。**

    當程式將列印工作傳送至印表機，或使用者已取消列印工作之後，您必須關閉列印工作，並釋放列印工作所使用的資源。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何：收集使用者的列印工作資訊](preparing-to-print.md)
</dt> </dl>

 

 
