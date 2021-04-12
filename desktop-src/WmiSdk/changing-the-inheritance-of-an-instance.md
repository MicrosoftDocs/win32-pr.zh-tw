---
description: 您可能會發現，建立為一個父類別之子系的實例必須變更父類別，並成為不同父類別的子系。
ms.assetid: 6d0fd456-81ab-4665-bb88-f9fb29fbbd39
ms.tgt_platform: multiple
title: 變更實例的繼承
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a35de3dcc37d91b318ab60fb5a520cb4da10e59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849570"
---
# <a name="changing-the-inheritance-of-an-instance"></a>變更實例的繼承

您可能會發現，建立為一個父類別之子系的實例必須變更父類別，並成為不同父類別的子系。 例如，您可能有衍生類別 **ManualService**、描述手動服務，以及描述自動服務的衍生類別 **AutoService**。 這兩個類別都有許多屬性。 並非所有屬性都相同。 若要將服務從手動變更為自動，您也必須將代表服務的實例從 **ManualService** 變更為 **AutoService**。 在目前的 WMI 版本中，您無法呼叫 [**IWbemServices：:P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) 方法，並將 *PInst* 參數指向 **AutoService** 的實例，以及描述 **ManualService** 實例的索引鍵屬性。 如果您這麼做，就會隱含地刪除原始的 **ManualService** 實例。 基本上，在建立實例的類別之後，您只能藉由刪除實例並重新建立實例作為新父類別的實例，來變更實例的父類別。

下列程式描述如何將實例從某個類別移至另一個類別。

**將實例從一個類別移至另一個類別**

1.  從原始類別中刪除實例。
2.  在新類別下建立實例。

    WMI 不允許應用程式在新的類別中建立實例來移動實例，然後使用原始實例的金鑰來更新它。

如需詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md)。

 

 



