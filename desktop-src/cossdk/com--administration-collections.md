---
description: COM + 系統管理集合可保存和組織 COM + 目錄中所儲存的設定資料。
ms.assetid: eed8ca97-39ad-4188-afc6-8670b5073fad
title: COM + 系統管理集合
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceb49ecd382e5a5a570e3e479714ad905a5eaf5f
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/03/2021
ms.locfileid: "104561129"
---
# <a name="com-administration-collections"></a>COM + 系統管理集合

COM + 系統管理集合可保存和組織 COM + 目錄中所儲存的設定資料。 集合會對應至元件服務管理工具的主控台樹中的資料夾。 您可以使用 COM + 系統管理物件和介面來存取這些集合。

您可以使用從 [**COMAdminCatalog**](comadmincatalog.md) 類別建立的物件起始程式設計管理、使用從 [**COMAdminCatalogCollection**](comadmincatalogcollection.md) 類別建立的物件來表示目錄中的任何集合，而且您可以使用從 [**COMAdminCatalogObject**](comadmincatalogobject.md) 類別建立的物件來表示集合中的專案。

指定集合中的專案會公開一組一致的屬性。 例如， [**元件**](components.md) 集合中的每個專案都代表一個元件，而 **元件** 集合中的專案則會公開用來設定元件的相同屬性。 您可以使用 [**COMAdminCatalogObject**](comadmincatalogobject.md) 類別來存取這些屬性。

> [!Note]  
> 具有 WriteOnce 存取權的屬性為 ReadWrite，在使用 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)之前使用 [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add)方法，且之後為 ReadOnly。

 

如需以程式設計方式管理 COM + 的簡介，請參閱 [自動化 COM + 管理](automating-com--administration.md)。

## <a name="collection-hierarchy"></a>集合階層

下圖說明集合之間的關聯性。 在白色和灰色) 方塊中，最左邊 (的集合是最上層的集合，可呼叫從 [**COMAdminCatalog**](comadmincatalog.md)類別建立之物件的 [**>getcollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection)方法來存取。 您可以透過呼叫代表其父系之 [**COMAdminCatalogCollection**](comadmincatalogcollection.md)物件的 [**>getcollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection)方法，在黃色方塊中 (剩餘的集合，) 只能透過其父代集合來存取它們。 箭號會從父集合指向其子集合。

![顯示集合之間關聯性的圖表。](images/ab61b0ab-2368-4bd8-9cfc-b7adc5beaca3.png)

圖中未說明下列四個集合： [**ErrorInfo**](errorinfo.md)、 [**PropertyInfo**](propertyinfo.md)、 [**RelatedCollectionInfo**](relatedcollectioninfo.md)和 [**Root**](root.md)。 **ErrorInfo** 集合是圖形中每個集合的子系，但 [**InprocServers**](inprocservers.md)和 [**WOWInprocServers**](wowinprocservers.md) (在灰色方塊中) 。 **PropertyInfo** 和 **RelatedCollectionInfo** 集合是每個集合的子系。 **根** 集合是最上層集合，它是所有其他最上層集合的父系。 不過，存取其他最上層集合之前，不需要先存取 **根** 集合。

## <a name="comadmin-library"></a>COMAdmin 程式庫

COMAdmin 程式庫支援下列集合。



| 集合                                                             | Description                                                                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplicationCluster**](applicationcluster.md)                       | 包含應用程式叢集中的伺服器清單。                                                                                            |
| [**ApplicationInstances**](applicationinstances.md)                   | 針對正在執行的 COM + 應用程式的每個實例，各包含一個物件。                                                                                   |
| [**應用程式**](applications.md)                                   | 針對安裝在本機電腦上的每個 COM + 應用程式，各包含一個物件。                                                                         |
| [**單元**](components.md)                                       | 針對應用程式中與它相關的每個元件，各包含一個物件。                                                                      |
| [**ComputerList**](computerlist.md)                                   | 包含在 [元件服務] 系統管理工具的 [ **電腦** ] 資料夾中找到的電腦清單。                                     |
| [**DCOMProtocols**](dcomprotocols.md)                                 | 包含 DCOM 要使用的通訊協定清單。 它包含每個通訊協定的物件。                                                         |
| [**ErrorInfo**](errorinfo.md)                                         | 抓取有關處理多個物件之方法的延伸錯誤資訊。                                                               |
| [**EventClassesForIID**](eventclassesforiid.md)                       | 捕獲事件類別的相關資訊。                                                                                                        |
| [**FilesForImport**](filesforimport.md)                               | 從它的 MSI 檔案抓取可匯入之應用程式的相關資訊。                                                                    |
| [**InprocServers**](inprocservers.md)                                 | 包含向系統註冊的同進程伺服器清單。 它包含每個元件的物件。                                       |
| [**InterfacesForComponent**](interfacesforcomponent.md)               | 針對集合所關聯的元件所公開的每個介面，各包含一個物件。                                                    |
| [**LegacyComponents**](legacycomponents.md)                           | 針對應用程式中每個未設定的元件，包含與其相關的物件。                                                         |
| [**LegacyServers**](legacyservers.md)                                 | 與 [**InprocServers**](inprocservers.md) 集合相同，不同之處在于此集合也包含本機伺服器。                           |
| [**LocalComputer**](localcomputer.md)                                 | 包含單一物件，該物件會保存您要存取其目錄之電腦的電腦層級設定資訊。                             |
| [**MethodsForInterface**](methodsforinterface.md)                     | 針對與集合相關的介面上的每個方法，各包含一個物件。                                                               |
| [**分區**](partitions.md)                                       | 用來指定每個分割區中包含的應用程式。                                                                                         |
| [**PartitionUsers**](partitionusers.md)                               | 用來指定每個資料分割中包含的使用者。                                                                                                |
| [**PropertyInfo**](propertyinfo.md)                                   | 抓取指定集合所支援之屬性的相關資訊。                                                                      |
| [**PublisherProperties**](publisherproperties.md)                     | 包含父 [**SubscriptionsForComponent**](subscriptionsforcomponent.md) 集合之每個發行者屬性的物件。              |
| [**RelatedCollectionInfo**](relatedcollectioninfo.md)                 | 抓取與所呼叫之集合相關的其他集合相關資訊。                                                      |
| [**角色**](roles.md)                                                 | 針對指派給與其相關聯之應用程式的每個角色，各包含一個物件。                                                                  |
| [**RolesForComponent**](rolesforcomponent.md)                         | 針對指派給集合相關之元件的每個角色，各包含一個物件。                                                        |
| [**RolesForInterface**](rolesforinterface.md)                         | 針對指派給集合所關聯之介面的每個角色，各包含一個物件。                                                        |
| [**RolesForMethod**](rolesformethod.md)                               | 針對指派給集合相關之方法的每個角色，各包含一個物件。                                                           |
| [**RolesForPartition**](rolesforpartition.md)                         | 針對指派給集合相關之分割區的每個角色，各包含一個物件。                                                        |
| [**根**](root.md)                                                   | 包含目錄上的最上層集合。                                                                                                    |
| [**SubscriberProperties**](subscriberproperties.md)                   | 包含父 [**SubscriptionsForComponent**](subscriptionsforcomponent.md) 集合之每個訂閱者屬性的物件。             |
| [**SubscriptionsForComponent**](subscriptionsforcomponent.md)         | 包含父 [**元件**](components.md) 集合之每個訂用帳戶的物件。                                                  |
| [**TransientPublisherProperties**](transientpublisherproperties.md)   | 包含父 [**TransientSubscriptions**](transientsubscriptions.md) 集合之每個發行者屬性的物件。                    |
| [**TransientSubscriberProperties**](transientsubscriberproperties.md) | 包含父 [**TransientSubscriptions**](transientsubscriptions.md) 集合之每個訂閱者屬性的物件。                   |
| [**TransientSubscriptions**](transientsubscriptions.md)               | 包含每個暫時性訂用帳戶的物件。                                                                                                   |
| [**UsersInPartitionRole**](usersinpartitionrole.md)                   | 針對分割區角色中與集合相關的每個使用者，各包含一個物件。                                                            |
| [**UsersInRole**](usersinrole.md)                                     | 針對與集合相關的角色中的每個使用者，各包含一個物件。                                                                      |
| [**WOWInprocServers**](wowinprocservers.md)                           | 包含在64位電腦上向系統註冊32位元件的同進程伺服器清單。                                       |
| [**WOWLegacyServers**](wowlegacyservers.md)                           | 與 [**LegacyServers**](legacyservers.md) 集合相同，不同之處在于此集合是在64位電腦上的32位登錄中繪製。 |



 

 

 



