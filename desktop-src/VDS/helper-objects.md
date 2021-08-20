---
description: VDS 會提供兩個 helper 物件：列舉物件和 async 物件。 本主題將說明每個物件，並提供呼叫端如何與每個物件搭配使用的範例連結。
ms.assetid: 0f809c71-a3bd-4c62-8086-9651ea1a3400
title: Helper 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98464c31548309b50e21b2b8e3e20a867efe7ca647d7a9879efd0ef346e6a147
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999478"
---
# <a name="helper-objects"></a>Helper 物件

\[從 Windows 8 和 Windows Server 2012 開始， [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)會取代[虛擬磁碟服務](virtual-disk-service-portal.md)COM 介面。\]

VDS 會提供兩個 helper 物件：列舉物件和 async 物件。 本主題將說明每個物件，並提供呼叫端如何與每個物件搭配使用的範例連結。

## <a name="enumeration-object"></a>列舉物件

列舉物件會透過指定類型的一組 VDS 物件來列舉。 物件可以是提供者、子系統、控制器、Lun、LUN 的 plex、磁片磁碟機、磁片套件、磁片、磁片區或磁片區的 plex。 呼叫端可以從適當方法所傳回的列舉中選取所需的物件，以取得特定物件的指標。 如需程式碼範例，請參閱 [使用列舉物件](working-with-enumeration-objects.md)。

下表列出相關的介面、列舉和結構。 

| 類型                                              | 元素                                  |
|---------------------------------------------------|------------------------------------------|
| 一律由這個物件公開的介面 | [**IEnumVdsObject**](/windows/desktop/api/Vds/nn-vds-ienumvdsobject) |
| 相關聯的列舉                           | 無。                                    |
| 相關聯的結構                             | 無。                                    |



 

## <a name="async-object"></a>Async 物件

非同步物件會管理非同步作業。 起始非同步作業的方法會傳回指向 [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) 介面的指標，讓呼叫端可以取消、等候和查詢非同步作業的狀態。

長時間執行的 VDS 作業通常會以非同步方式執行。 基本和動態軟體提供者程式會以一致的方式執行磁片區、磁碟分割和磁片作業的非同步方法。 硬體提供者可選擇以非同步方式執行非同步相關的方法。 不論提供者如何執行方法，作業都必須將 [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) 介面的指標傳回給呼叫者。 如需程式碼範例，請參閱 [管理非同步作業](managing-asynchronous-operations.md)。

非同步作業包括：

-   建立 LUN、磁片區或磁碟分割。
-   格式化磁片區或磁碟分割。
-   新增或移除 LUN 或磁片區 plex。
-   中斷磁片區 plex。
-   擴充或壓縮 LUN 或磁片區。
-   復原 LUN 或磁片區。
-   清理磁片。
-   更換磁片。

下表列出相關的介面、列舉和結構。 

| 類型                                              | 元素                        |
|---------------------------------------------------|--------------------------------|
| 一律由這個物件公開的介面 | [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) |
| 相關聯的列舉                           | 無。                          |
| 相關聯的結構                             | 無。                          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[VDS 物件模型](vds-object-model.md)
</dt> <dt>

[**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync)
</dt> <dt>

[使用列舉物件](working-with-enumeration-objects.md)
</dt> <dt>

[管理非同步作業](managing-asynchronous-operations.md)
</dt> </dl>

 

 
