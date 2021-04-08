---
title: 動態注釋的類型
description: Microsoft Active Accessibility 直接批註、值對應注釋和伺服器批註支援三種類型的動態注釋。 每種類型都提供特定的優點，因此請務必瞭解差異。
ms.assetid: 113fea65-982e-4291-9d60-bbb57282f3f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0453d3b5d05e2713d1a57fb0f475d4ec2a481b02
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840040"
---
# <a name="types-of-dynamic-annotation"></a>動態注釋的類型

Microsoft Active Accessibility 中支援三種動態注釋類型： *直接批註*、 *值對應注釋* 和 *伺服器注釋*。 每種類型都提供特定的優點，因此請務必瞭解差異。

## <a name="direct-annotation"></a>直接注釋

直接注釋是動態注釋最簡單的形式。 它最適用于批註屬性不相依于控制項狀態的可存取專案，而且不需要由值對應注釋和伺服器批註提供的額外支援。 直接批註是用來覆寫可存取專案的一或多個 Microsoft Active Accessibility 屬性的值，以及覆寫或加入 Microsoft 消費者介面自動化屬性至控制項。 Microsoft Active Accessibility 屬性中所做的所有批註都會反映在消費者介面自動化轉譯和 Microsoft Active Accessibility 對消費者介面自動化 proxy 中。 如需詳細資訊，請參閱 [直接批註](direct-annotation.md)。

## <a name="value-map-annotation"></a>值對應注釋

除了直接批註 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性以外，通常還需要將控制項特定的值轉換成可由使用者理解的字串。 例如，在 [設定] 索引標籤的 [**設定**] 索引標籤下的 [螢幕解析度] 滑杆控制項， (**主控台**) 的 **顯示內容**。 雖然每個滑杆位置都對應至不同的解析度 (例如，640 x 480、1024 x 768) 、控制項並不知道此關聯性，也無法將這項資訊傳遞給 Microsoft Active Accessibility。

值對應批註可讓這項工作更容易。 您可以使用這種形式的注釋來指定滑杆值的字串，並指定清單和樹狀檢視中圖示的角色、狀態和描述。 如需詳細資訊，請參閱 [值對應注釋](value-map-annotation.md)。

## <a name="server-annotation"></a>伺服器注釋

伺服器批註可讓開發人員註冊回呼物件，以服務用戶端對專案標注屬性的要求。 此回呼物件必須執行 [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver) 介面，並向 Microsoft Active Accessibility 注釋服務註冊。 註冊之後，系統會要求您針對該可存取專案的屬性值服務所有用戶端要求。

伺服器批註的一個特別有用的功能是，可以註冊一次伺服器來處理容器及其所有子系的要求。 比方說，單一伺服器可以設定一次，以處理所有專案的要求是一個清單方塊。 如需詳細資訊，請參閱 [伺服器注釋](server-annotation.md)。

 

 




