---
description: 在 COM + 中，物件的共用暫時性狀態是使用共用屬性管理員 (SPM) 來管理。 SPM 是一個資源配置器，可讓您用來在伺服器進程內的多個物件之間共用狀態。
ms.assetid: 31b50c2a-68b5-4816-9a56-8cd9475e7beb
title: COM + 共用屬性管理員概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9be55c4a83aa363c911564aefabbe1d85f3804fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970340"
---
# <a name="com-shared-property-manager-concepts"></a>COM + 共用屬性管理員概念

在 COM + 中，物件的共用暫時性狀態是使用共用屬性管理員 (SPM) 來管理。 SPM 是一個資源配置器，可讓您用來在伺服器進程內的多個物件之間共用狀態。

因為並行和名稱衝突的問題，所以您無法在分散式環境中使用全域變數。 共用屬性管理員會藉由提供共用屬性群組來消除名稱衝突，而這些群組會為其所包含的共用屬性建立唯一的命名空間。 SPM 也會執行鎖定和信號，以協助保護共用屬性免于同時存取，這可能會導致更新遺失並讓屬性處於無法預測的狀態。

> [!Note]  
> 共用的暫時性狀態是保留在記憶體中的狀態資訊，而這些資訊不會在系統失敗時存活。 這項資訊是設計成跨交易 (的多個物件共用，但不能跨進程) 界限共用。

 

儲存在 SPM 中的共用屬性僅適用于在相同進程中執行的物件。 這表示將使用 SPM 儲存值的物件，以及需要存取這些值的物件，都必須安裝為相同 COM + 應用程式的一部分。 當您的 COM + 應用程式部署完成後，系統管理員可以將 COM + 類別從一個套件移至另一個套件。 如果您依賴數個透過 SPM 共用屬性的物件，您應該清楚記載必須將它們安裝在相同的 COM + 應用程式中。

共用屬性的元件也必須具有相同的啟用屬性。 如果相同封裝中的兩個元件有不同的啟用屬性，它們通常無法共用屬性。 例如，如果某個元件設定為在用戶端進程中執行，而另一個元件設定為在伺服器進程中執行，則它們的物件通常會在不同的進程中執行，即使它們是在相同的封裝中也一樣。

您應該一律從 COM + 元件具現化 [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md)、 [**SharedPropertyGroup**](sharedpropertygroup.md)和 [**SharedProperty**](sharedproperty.md) 物件，而不是從基底用戶端。 如果基底用戶端建立共用屬性群組和屬性，共用屬性就會在基底用戶端進程內，而不是在伺服器進程中。 這表示，除非物件也在用戶端進程中執行，否則 COM + 物件無法共用屬性 (這通常不是很好的想法) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 共用屬性管理員](com--shared-property-manager.md)
</dt> <dt>

[共用屬性群組](shared-property-groups.md)
</dt> </dl>

 

 



