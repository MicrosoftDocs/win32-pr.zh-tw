---
description: 802.1 X 設定檔包含下列架構元素。
ms.assetid: be3f1986-d0c2-47f6-b4dd-8defb89bd03a
title: OneX 架構元素
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7b7f3e7bac256b915d0e134720fc63b3519b21e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692947"
---
# <a name="onex-schema-elements"></a>OneX 架構元素

802.1 X 設定檔包含下列架構元素。 所有的 OneX 架構元素都適用于有線和無線設定檔。 `https://www.microsoft.com/networking/OneX/v1`除了命名空間中的 [**EAPConfig (OneX)**](onexschema-eapconfig-onex-element.md)之外，大部分的命名元素都位於命名空間中 `https://www.microsoft.com/provisioning/EapHostConfig` 。

下列清單以專案在設定檔中出現的順序顯示已定義的元素。 強制執行元素的順序。 並非所有專案都在每個設定檔中，因為有些元素是選擇性的。

這份清單不會顯示所有可能出現在設定檔中的元素，因為可以在 **xs：任何** 插入點中加入元素。

-   [**OneX**](onexschema-onex-element.md)
    -   [**cacheUserData (OneX)**](onexschema-cacheuserdata-onex-element.md)
    -   [**heldPeriod (OneX)**](onexschema-heldperiod-onex-element.md)
    -   [**authPeriod (OneX)**](onexschema-authperiod-onex-element.md)
    -   [**startPeriod (OneX)**](onexschema-startperiod-onex-element.md)
    -   [**maxStart (OneX)**](onexschema-maxstart-onex-element.md)
    -   [**maxAuthFailures (OneX)**](onexschema-maxauthfailures-onex-element.md)
    -   [**supplicantMode (OneX)**](onexschema-supplicantmode-onex-element.md)
    -   [**authMode (OneX)**](onexschema-authmode-onex-element.md)
    -   [**singleSignOn (OneX)**](onexschema-singlesignon-onex-element.md)
        -   [**輸入 (singleSignOn)**](onexschema-type-singlesignon-element.md)
        -   [**maxDelay (singleSignOn)**](onexschema-maxdelay-singlesignon-element.md)
        -   [**userBasedVirtualLan (singleSignOn)**](onexschema-userbasedvirtuallan-singlesignon-element.md)
    -   [**EAPConfig (OneX)**](onexschema-eapconfig-onex-element.md)

 

 



