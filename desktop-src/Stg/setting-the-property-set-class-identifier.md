---
title: 設定屬性集類別識別碼
description: IPropertyStorage SetClass 方法會設定儲存物件的 CLSID 和儲存在 COM 屬性集中的類別標記值。 當在儲存于結構化儲存物件中的簡單屬性儲存體上叫用時，就會發生這種情況。
ms.assetid: 3f542a66-5e04-43c1-a386-7d709c615972
keywords:
- 設定屬性集類別識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f9ec6e038ef6bc5f4f12228581946a4051c532b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021889"
---
# <a name="setting-the-property-set-class-identifier"></a>設定屬性集類別識別碼

[**IPropertyStorage：： SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)方法會設定儲存物件的 CLSID 和儲存在 COM 屬性集中的類別標記值。 當在儲存于結構化儲存物件中的簡單屬性儲存體上叫用時，就會發生這種情況。

這可提供一致性和一致性，進而與某些工具產生更佳的互動。 如果屬性儲存物件是藉由呼叫 [**IPropertySetStorage：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) 並設定 **PROPSETFLAG \_ 簡單** 旗標所建立，就會簡單。

儲存物件的 CLSID 是透過呼叫 [**IStorage：： SetClass**](/windows/desktop/api/Objidl/nf-objidl-istorage-setclass)來設定。

 

 




