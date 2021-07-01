---
description: 請參閱有關檔和列印功能和選項的使用者介面行為討論。
ms.assetid: dc19a568-3673-4061-b19a-50d5df0485d0
title: 消費者介面行為
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e81d007c653ed3f019892e944d9fa4203dc6de11
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119433"
---
# <a name="user-interface-behavior"></a>消費者介面行為

本主題並非最新的。 如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。

假設您要建立的 PrintCapabilities 用戶端會讀取 PrintCapabilities 檔，並從每個功能中選取一個或多個選項，並使用這些選項來建立 PrintTicket，以指定要用來處理作業的設定。 針對每個感興趣的功能，用戶端必須檢查每個選項，並決定該選項是否適合手邊的工作。 針對未參數化的選項，可以藉由存取每個 ScoredProperty 的值來進行評估。 在 nonparameterized 媒體大小選項的案例中，用戶端會決定每個選項所報告之媒體的寬度和高度維度是否符合所需的維度。

在參數化選項的情況下，用戶端必須存取其中一個 ScoredProperty 實例中所包含之 ParameterRef 實例中所指出的 ParameterDef 實例。 ParameterDef 通常會定義參數所允許的值範圍，以及單位 (英寸、mm 等) 以值表示。 如果必要的維度落在每個參數允許的值範圍內，則用戶端會透過 PrintTicket 中) 的 ParameterInit 實例來初始化參數 (的額外工作。 這是特別重要的工作。 例如，在不指定媒體的維度的情況下，PrintTicket 不應指定自訂媒體大小，因為產生的 PrintTicket 將會不明確且定義錯誤。

如果用戶端是使用者介面，則必須處理一組類似的情況。 使用者介面通常會顯示針對每個選項所定義的 ScoredProperty 實例值。 為了清楚起見，在參數化選項中顯示參數的允許範圍和單位是很重要的。 此外，如果使用者選取參數化選項，使用者介面 (UI) 必須提示使用者輸入要用來初始化每個參數的值。 最後，UI 必須撰寫可反映所有使用者選取專案的 PrintTicket。

如需 PrintTicket 結構和參數初始化規格的詳細資料，請參閱 [建立 Device-Specific printticket](creating-a-device-specific-printticket.md)。 如需有關 ParameterRef 實例的取值以及解讀 ParameterDef 實例的詳細資訊，請參閱 [使用參數](using-parameters.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



