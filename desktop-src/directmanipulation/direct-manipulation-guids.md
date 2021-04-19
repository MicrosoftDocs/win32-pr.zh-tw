---
description: 下列直接操作類別 Guid 定義于 DirectManipulation 中。
ms.assetid: 6747D082-4B7B-4C7E-A230-2E8C8412FABD
title: 直接操作 Guid
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 57dfa5701d7f01a9738206e7a2e3d669f6cf6a4a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973741"
---
# <a name="direct-manipulation-guids"></a>直接操作 Guid

下列 [直接操作](direct-manipulation-portal.md) 類別 guid 定義于 DirectManipulation 中。

- [主要類別識別碼](#master-class-ids)
- [次要內容類別別-識別碼](#secondary-content-class-ids)
- [行為物件類別識別碼](#behavior-objects-class-ids)
- [相關主題](#related-topics)

## <a name="master-class-ids"></a>主要類別識別碼

| GUID                                     | Description                                                                                                                                                                                                                                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **54E211B6-3650-4F75-8334-FA359598E1C5** | DirectManipulationManager 類別。 此物件可讓您存取應用程式可用的所有 [直接操作](direct-manipulation-portal.md) 功能和 api。                                                                                                                         |
| **79DEA627-A08A-43AC-8EF5-6900B9299126** | DCompManipulationCompositor 類別。 這是包裝 DirectComposition 的 [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor) 執行。 透過這個組合器物件 DirectManipulation 可以直接在 DComp 樹狀結構上設定轉換來套用輸出。 |

## <a name="secondary-content-class-ids"></a>次要內容類別別-識別碼

| GUID                                  | Description                                                                                                                      |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| **CLSID \_ VerticalIndicatorContent**   | 垂直移動指標。 視覺專案，顯示內容中，垂直擴充的目前位置。     |
| **CLSID \_ HorizontalIndicatorContent** | 水準移動指標。 視覺專案，顯示內容中水準擴充的目前位置。 |
| **CLSID \_ VirtualViewportContent**     | 虛擬區。 虛擬區可以用來針對已設定縮放比例的各區，使用固定的位置元素。          |

## <a name="behavior-objects-class-ids"></a>行為物件類別識別碼

| GUID                                     | Description                                                                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CLSID \_ DragDropConfigurationBehavior** | 拖曳 & Drop 行為。 啟用選取和拖曳專案。                                                                                       |
| **CLSID \_ AutoScrollBehavior**            | Autoscroll 行為。 讓內容在接近指定軸的界限時自動滾動。                                           |
| **CLSID \_ DeferContactService**           | 聯絡延遲行為。 在呼叫 [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact)之前，millliseconds) 等候的時間量 (。 |

## <a name="related-topics"></a>相關主題

[Direct 操作](direct-manipulation-portal.md)、 [**ActivateConfiguration**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-activateconfiguration)、 [**AddConfiguration**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-addconfiguration)、 [**IDirectManipulationCompositor**](/windows/win32/api/DirectManipulation/nn-directmanipulation-idirectmanipulationcompositor)
