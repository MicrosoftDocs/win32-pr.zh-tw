---
description: 將磁碟機號新增至 LUN
ms.assetid: 3f350312-3f1f-4020-90d0-85521ea9c7c8
title: 將磁碟機號新增至 LUN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426a4f3bf720b21a02462edde4a381012d2084d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106997081"
---
# <a name="adding-a-drive-letter-to-a-lun"></a>將磁碟機號新增至 LUN

\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]

您可以直接將磁碟機號指派給磁片區物件;但是，如果您的磁片是 LUN 物件，您會有幾個額外的步驟。

**指派磁碟機號給 LUN 物件**

1.  如有必要，請將 LUN 取消遮罩至本機主機。
    > [!Note]  
    > 您無法對目前 VDS 會話內的另一部電腦取消遮罩的 LUN 物件執行軟體系統管理作業。

     

2.  在正在執行硬體提供者的電腦上叫用 [**IVdsService：： Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) 方法。
3.  將 LUN 初始化為基本磁碟，如下所示：
    1.  在 LUN 物件上叫用 [**IUnknown：： QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 方法，以查詢 [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) 介面。
    2.  叫用 [**IVdsSwProvider：： CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) 方法，以建立基本套件。
    3.  叫用 [**IVdsPack：： AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) 方法，將磁片新增至新的套件。
4.  在磁片上建立磁碟分割，並取得磁片區物件，如下所示：
    1.  叫用 [**IVdsCreatePartitionEx：： CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex) 方法來建立資料分割。
    2.  在 [**CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex)所傳回的非同步物件上叫用 [**IVdsAsync：： Wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait)方法，以從 [**VDS \_ 非同步 \_ 輸出**](/windows/desktop/api/Vds/ns-vds-vds_async_output)結構取得磁片區識別碼。
    3.  將磁片區識別碼作為參數傳遞給 [**IVdsService：： GetObject**](/windows/desktop/api/Vds/nf-vds-ivdsservice-getobject) 方法，以取得磁片區物件指標。
5.  叫用 [**IVdsVolumeMF：： AddAccessPath**](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath) 方法以指派磁碟機號。

> [!Note]  
> [**IVdsAdvancedDisk：： AssignDriveLetter**](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter)方法會將磁碟機號指派給沒有相關聯磁片區的磁碟分割，例如 OEM 或 ESP 磁碟分割。 您無法使用它來指派磁碟機號給 LUN 物件。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 VDS](using-vds.md)
</dt> <dt>

[**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)
</dt> <dt>

[**IVdsSwProvider::CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack)
</dt> <dt>

[**IVdsPack::AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk)
</dt> <dt>

[**IVdsCreatePartitionEx::CreatePartitionEx**](/windows/desktop/api/Vds/nf-vds-ivdscreatepartitionex-createpartitionex)
</dt> <dt>

[**IVdsAsync：： Wait**](/windows/desktop/api/Vds/nf-vds-ivdsasync-wait)
</dt> <dt>

[**VDS \_ 非同步 \_ 輸出**](/windows/desktop/api/Vds/ns-vds-vds_async_output)
</dt> <dt>

[**IVdsVolumeMF::AddAccessPath**](/windows/desktop/api/Vds/nf-vds-ivdsvolumemf-addaccesspath)
</dt> <dt>

[**IVdsAdvancedDisk::AssignDriveLetter**](/windows/desktop/api/Vds/nf-vds-ivdsadvanceddisk-assigndriveletter)
</dt> </dl>

 

 
