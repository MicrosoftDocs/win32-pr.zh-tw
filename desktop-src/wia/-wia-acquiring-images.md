---
description: 選取映射之後，應用程式會針對在 Windows XP 或) 舊版中執行的應用程式使用 IWiaDataTransfer 介面 (，或針對在 Windows Vista 或更新版本中執行的應用程式使用 IWiaTransfer 介面 () 從映射裝置傳輸影像資料。 如需詳細資訊，請參閱 WIA 1.0 中的傳送影像資料，或傳輸 WIA 2.0 中的影像資料。
ms.assetid: cf76e526-d63b-4ee5-ba3c-871f2051a82c
title: 取得映射
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d062cb370327311ad0c7d4f883344c05bb776f6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988811"
---
# <a name="acquiring-images"></a>取得映射

選取映射之後，應用程式會針對在 Windows XP 或) 舊版中執行的應用程式使用 [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) 介面 (，或針對在 windows Vista 或更新版本中執行的應用程式使用 [**IWiaTransfer**](-wia-iwiatransfer.md) 介面 () 從映射裝置傳輸影像資料。 如需詳細資訊，請參閱 [wia 1.0 中的傳送影像資料](-wia-transferring-image-data.md) ，或 [傳輸 wia 2.0 中的影像資料](-wia-transferring-image-data-in-wia2.md) 。

選取裝置之後，應用程式會使用裝置的 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)或 [**IWiaItem2**](-wia-iwiaitem2.md)介面的 [**IWiaItem：:D evicedlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg)方法， (根項目) 從指定的 Windows 映像取得 (WIA) 裝置選取影像。 [**IWiaDevMgr：： GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg)方法會顯示一個對話方塊，讓使用者可以從指定的裝置選取影像，並將影像傳送到使用者所選取的檔案名。 它也可讓使用者在必要時指定裝置。 如需詳細資訊，請參閱 [選取裝置](-wia-selecting-a-device.md)

請注意，使用者不需要使用上述方法來選取影像。 應用程式可以直接從裝置的專案樹狀結構取得影像專案的指標。 如需相關指示，請參閱 [導覽專案樹狀結構](-wia-navigating-an-item-tree.md)。

選取代表所需影像的 WIA 專案之後，在 Windows XP 或更早版本上執行的應用程式會查詢該專案的 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) 介面，以取得其 [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) 介面的指標。 在 Windows Vista 或更新版本上執行的應用程式會查詢其 [**IWiaTransfer**](-wia-iwiatransfer.md)介面指標的 [**IWiaItem2**](-wia-iwiaitem2.md)介面。

然後，應用程式可以使用 [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) (或 [**IWiaTransfer**](-wia-iwiatransfer.md)) 介面的方法，將影像資料傳輸至應用程式。

如果映射裝置是掃描器、 [**IWiaDataTransfer：： idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata)或 [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) 介面的其他方法，則會觸發掃描工作，然後傳送產生的影像資料。 如果裝置是相機，則影像資料只會從相機傳送至應用程式。

 

 



