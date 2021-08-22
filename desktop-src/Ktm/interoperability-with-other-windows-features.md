---
description: 分散式交易協調器 (DTC) 可在一或多個系統上控制多個資源管理員的分散式交易或交易。 KTM 和 DTC 密切合作以達成此目的。
ms.assetid: 468379e2-c5f6-479f-9d5d-42afb395ec9b
title: 與其他 Windows 功能的互通性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a18595140676539c6e5acaa5fc62835ac279215d068834e3e56dffe50d01e0e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119265068"
---
# <a name="interoperability-with-other-windows-features"></a>與其他 Windows 功能的互通性

[分散式交易協調器](/previous-versions/windows/desktop/ms684146(v=vs.85)) (DTC) 可在一或多個系統上控制多個資源管理員的 *分散式交易* 或交易。 KTM 和 DTC 密切合作以達成此目的。

COM + 會公開交易式程式設計的宣告式模型。 換句話說，程式設計人員會宣告物件可利用交易的範圍，而 COM + 執行時間代表物件管理交易。 例如，您只能將物件宣告為參與交易（如果已經存在的話），若要要求交易 (則會建立交易（如果它不 () 存在的話），而不論是否已存在) 或非交易式都會建立一個交易。 這些以宣告方式管理的交易會自動用於在交易內容中執行的 COM + 物件所建立的資料庫連接上。

 

 
