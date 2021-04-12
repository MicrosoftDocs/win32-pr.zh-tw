---
description: VDS 物件模型
ms.assetid: e5fcc19a-e170-4918-85eb-c1457776795a
title: VDS 物件模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae998955c5d0b7834cf4d88b901537f3644a2ab
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/04/2021
ms.locfileid: "104195646"
---
# <a name="vds-object-model"></a>VDS 物件模型

\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]

VDS 可間接存取以主機為基礎的存放裝置，例如磁片和 CD-ROM 裝置，以及由硬體 RAID 控制器管理的磁碟陣列。 某些儲存體實體會建立實體裝置模型、其他模型虛擬結構：磁片區、磁碟分割等等。 本主題所描述的物件代表 VDS 的實體和虛擬實體。

應用程式會呼叫這些物件所公開的方法，而 VDS 會呼叫適當的提供者來執行要求的儲存體作業。 應用程式永遠不會直接呼叫提供者程式。

### <a name="classification-of-objects"></a>物件分類

如下圖所示，軟體提供者程式會執行以主機為基礎之實體模型的物件;硬體提供者程式會執行模型內部和外部硬體 RAID 裝置的物件;其餘的一般物件是提供者獨立的，或是由 VDS 所執行。 主軸（不是 VDS 物件）是由磁片或磁片區延伸組成的一般儲存體媒體的一詞。

![顯示物件分類的圖表，定義為「通用物件」、「軟體提供者物件」和「硬體提供者物件」。](images/vdsobjectmodel.png)

若要深入瞭解每個物件的行為，請從下列主題中選取：

-   服務載入器和服務物件，請參閱 [啟動和服務物件](startup-and-service-objects.md)。
-   列舉和非同步物件，請參閱 [Helper 物件](helper-objects.md)。
-   提供者物件，請參閱 [提供者物件](provider-object.md)。
-   套件、磁片、磁片區和磁片區 plex 物件，請參閱 [軟體提供者物件](software-provider-objects.md)。
-   子系統、控制器、磁片磁碟機、LUN 和 LUN plex 物件，請參閱 [硬體提供者物件](hardware-provider-objects.md)。

### <a name="object-creation"></a>建立物件

與物件建立相關聯的設定和查詢作業可能需要相當長的時間才能完成;因此，VDS 會以非同步方式叫用所有方法。 探索提供者會傳回所有完成、錯誤或狀態變更事件。 軟體提供者也會記錄所有錯誤和重大狀態變更。

### <a name="object-deletion"></a>刪除物件

有幾個 VDS 方法會刪除或轉換 VDS 物件。 呼叫端可以在方法傳回之後，透過介面指標來保存參考至已刪除的物件。 當呼叫端釋放介面時，VDS 會刪除物件。

關於刪除物件，呼叫端應該避免叫用這些介面上的 [**IUnknown：： Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 方法以外的任何內容。 提供者必須夠健全，才能處理不當呼叫端;如果呼叫端在已刪除的物件上叫用方法，則提供者應該傳回 **\_ \_ \_ 已刪除的 VDS E 物件**。

### <a name="service-initialization"></a>服務初始化

VDS 會為服務載入器和服務物件提供 (Clsid) 的類別識別碼，但只有服務載入器 Clsid 是公用的。 當提供者、呼叫的應用程式和服務執行下列工作時，就會進行服務初始化：

-   每個新的提供者會在安裝期間叫用 [**IVdsAdmin：： RegisterProvider**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsadmin-registerprovider) 方法，以向 VDS 註冊。 呼叫會在系統 hive 下建立登錄機碼，此登錄機碼是由提供者的物件 GUID 所識別。 包含在此機碼底下的是提供者物件的 Clsid、名稱、版本，以及提供者的版本 GUID。
    > [!Note]  
    > 提供者物件 Guid 是永久性的;軟體和硬體物件 Guid 不是。

     

-   應用程式會呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 函數，並將服務載入器 Clsid 傳遞為引數。 使用服務載入器物件的指標時，應用程式可以將所需的電腦名稱稱做為參數傳遞至 [**IVdsServiceLoader：： LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice) 方法，以從本機或遠端啟動 VDS。
-   當初始應用程式附加至服務時，VDS 會先在登錄機碼下找到的每個 Clsid 上呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，然後在每個提供者上呼叫 [**IVdsProviderPrivate：： OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload) 方法來初始化程式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 VDS](about-vds.md)
</dt> <dt>

[**IVdsAdmin：： RegisterProvider**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsadmin-registerprovider)
</dt> <dt>

[**IVdsServiceLoader::LoadService**](/windows/desktop/api/Vds/nf-vds-ivdsserviceloader-loadservice)
</dt> <dt>

[**IVdsProviderPrivate：： OnLoad**](/windows/desktop/api/VdsHwPrv/nf-vdshwprv-ivdsproviderprivate-onload)
</dt> </dl>

 

 
