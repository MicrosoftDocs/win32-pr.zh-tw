---
description: 同步處理管理員包含使用者介面元件，例如 SyncMgr 服務中的索引標籤式對話方塊、錯誤對話方塊和進度對話方塊。
title: 同步處理管理員架構
ms.topic: article
ms.date: 05/31/2018
ms.assetid: db338835-ca8d-4e9f-973a-8eb081feda2b
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 584329a06ee9df80558d9961b734b62a57d5ebccd83f200690812fa99132b06d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451864"
---
# <a name="synchronization-manager-architecture"></a>同步處理管理員架構

同步處理管理員包含使用者介面元件，例如 SyncMgr 服務中的索引標籤式對話方塊、錯誤對話方塊和進度對話方塊。 使用者介面元件可讓使用者排程同步處理的應用程式，並設定自動同步處理，以與指定的系統事件一起發生。 例如，您可以在使用者登入或系統關機時叫用 SyncMgr。 使用者也可以叫用手動同步處理。

使用者選取應用程式，並指定要同步處理之應用程式內的專案，並設定觸發程式事件。 例如，在電子郵件應用程式中，[收件匣]、[寄件匣] 或其他包含訊息的資料夾可以是應用程式的個別專案。

SyncMgr 也包含程式設計介面，讓應用程式可以註冊以使用同步處理功能、可處理錯誤，以及在同步處理過程中接收進度資訊和通知。

 

 



