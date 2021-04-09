---
title: 手動處理檔案傳輸
description: 手動處理檔案傳輸
ms.assetid: ff94191b-a0f2-4118-996c-d040f214fb9b
keywords:
- Windows Media 裝置管理員，手動檔案傳輸
- 裝置管理員，手動檔案傳輸
- 程式設計指南，手動檔案傳輸
- 桌面應用程式，手動檔案傳輸
- 建立 Windows Media 裝置管理員應用程式，手動檔案傳輸
- 手動檔案傳輸
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2bf12404e8cd83b6f0c0e4f1c8ec8b0b7bda205
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682767"
---
# <a name="handling-file-transfers-manually"></a>手動處理檔案傳輸

您的應用程式可以執行 [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) 介面，以管理部分的讀取或寫入處理常式。 在讀取裝置時，此實行可讓應用程式接收來自裝置檔案的原始資料區塊。 在寫入裝置時，它會讓應用程式將原始資料的區區塊轉送到裝置上的檔案。

在讀取和寫入作業中， [**IWMDMOperation：： TransferObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) 方法會在電腦與裝置之間傳遞資料。 若要知道資料傳輸的方向，當 Windows Media 裝置管理員呼叫 [**BeginRead**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginread) 或 [**BeginWrite**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginwrite)時，您的應用程式必須設定旗標。 當呼叫 [**End**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-end) 方法時，應用程式應該重設此旗標。

> [!Note]  
> 如果服務提供者和裝置正確地執行 [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2)，它會先呼叫應用程式的 [IWMDMOperation3：： TransferObjectDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation3-transferobjectdataonclearchannel) 方法（如果已執行）。 此方法是傳輸資料的更有效率方式。 **TransferObjectDataOnClearChannel** 的處理方式與 **TransferObjectData** 相同，不同之處在于資料永遠不會加密，而且不會有 MAC 值可進行驗證。

 

下列各節描述當您的應用程式執行 **IWMDMOperation** 時的讀取和寫入程式。

**從裝置讀取**

從裝置讀取檔案時，Windows Media 裝置管理員會依序呼叫下列 **IWMDMOperation** 方法：

-   [**BeginRead**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginread) 呼叫以通知應用程式正在開始讀取裝置。
-   [**TransferObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) 呼叫一次或多次。 下列步驟說明資料的處理方式：
    1.  **TransferObjectData** 會接收大小 *pdwSize* 位元組的緩衝區 *.pdata*、填入資料，以及使用 MAC 來確認傳入的資料。
    2.  應用程式會使用傳入的資料 MAC 來驗證傳入的參數。
    3.  應用程式會盡可能解密和讀取 *.pdata* 中的資料量，並修改 *pdwSize* 的傳回值，以指出實際讀取的位元組數目。
    4.  應用程式會使用 [**CSecureChannelClient：:D ecryptparam**](/previous-versions/bb231586(v=vs.85))來解密資料，並視需要加以儲存或使用。
    5.  **TransferObjectData** 傳回 S \_ OK。
    6.  Windows Media 裝置管理員會繼續呼叫 **TransferObjectData** ，直到應用程式讀取檔案中的所有資料，或應用程式傳回 WMDM \_ E \_ 使用者取消 \_ 以取消作業 (在這種情況下，讀取會取消，而 Windows Media 裝置管理員會呼叫 **End**) 。
-   [**結束**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-end) 呼叫以通知應用程式，讀取裝置已結束。

**寫入至裝置**

將檔案寫入裝置時，Windows Media 裝置管理員會依序呼叫下列 **IWMDMOperation** 方法：

-   [**GetObjectName**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectname) 呼叫以允許應用程式指定新儲存體的名稱。 只有當應用程式未在 **Insert** 方法中指定名稱時，才會呼叫這個方法。
-   [**GetObjectAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectattributes) 呼叫以允許應用程式在裝置上指定新儲存體的屬性。
-   [**BeginWrite**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginwrite) 呼叫以通知裝置的寫入即將開始。
-   [**GetObjectTotalSize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjecttotalsize) 呼叫以抓取要寫入至裝置的物件大小總計，以啟用傳輸的優化，以及提供 Windows Media 裝置管理員有機會在檔案對裝置而言太大時，取消傳輸。
-   [**TransferObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) 呼叫一次或多次。 下列步驟說明資料的處理方式：
    1.  **TransferObjectData** 會接收大小 *pdwSize* 位元組緩衝區的指標。
    2.  應用程式會取得要傳送至裝置的資料區塊，通常是從檔案讀取資料，並以最多 *pdwSize* 的位元組填滿接收的緩衝區。 如果有需要，它應該修改 *pdwSize* (，) 以反映已新增至緩衝區的位元組數目。
    3.  應用程式會建立所有方法參數的 MAC。
    4.  應用程式會使用 [**CSecureChannelClient：： EncryptParam**](/previous-versions/bb231587(v=vs.85))來加密緩衝區中的資料。
    5.  **TransferObjectData** 會傳回 \_ [確定] 以表示有更多資料，或 \_ 指定 FALSE 表示沒有其他資料。 如果應用程式傳回 WMDM \_ E \_ 使用者已 \_ 取消，則會取消寫入作業，而且 Windows Media 裝置管理員會呼叫 **End**。
    6.  只要應用程式傳回 [確定]，Windows Media 裝置管理員就會繼續呼叫 **TransferObjectData** \_ 。
-   [**結束**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-end) 呼叫以通知裝置寫入正在結束。

如需程式碼範例，請參閱 [加密和解密](encryption-and-decryption.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立 Windows Media 裝置管理員應用程式**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 