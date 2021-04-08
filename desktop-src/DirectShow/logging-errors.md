---
description: 記錄錯誤
ms.assetid: 690ea91b-5bc0-45f0-8354-ec625709f7bd
title: 記錄錯誤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76cded9d4cfaedd93e846fec52b07bf5d4eef9a5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687663"
---
# <a name="logging-errors"></a>記錄錯誤

\[此 API 不受支援，而且可能會在未來變更或無法使用。\]

 (DES) 的[DirectShow 編輯服務](directshow-editing-services.md)提供內建機制，可記錄載入、建立或轉譯 DES 專案時所發生的錯誤。 本文提供範例主控台應用程式，此應用程式會載入 XML 專案檔，並嘗試加以呈現。 如果發生錯誤，應用程式會在主控台視窗中列印錯誤訊息。 本文所提供的範例程式碼是以 [載入和預覽專案](loading-and-previewing-a-project.md)時所提供的範例為基礎。

> [!Note]  
> 您的應用程式不需要執行錯誤記錄。 除非您明確要求，否則 DES 不會記錄錯誤。

 

本文假設您瞭解 COM 用戶端程式設計和 DES 時間軸模型。 此外，您還需要瞭解 COM 物件程式設計的基本概念。 如需 DES 中時間軸的詳細資訊，請參閱 [時間軸模型](the-timeline-model.md)。

本文包含下列各節。

-   [錯誤記錄總覽](overview-of-error-logging.md)
-   [建立錯誤記錄類別](creating-an-error-logging-class.md)
-   [執行 IAMErrorLog](implementing-iamerrorlog.md)
-   [設定錯誤記錄檔](setting-the-error-log.md)
-   [DES 錯誤記錄：範例程式碼](des-error-logging--example-code.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 DirectShow 編輯服務](using-directshow-editing-services.md)
</dt> </dl>

 

 



