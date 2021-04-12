---
description: 將外部磁片新增至套件
ms.assetid: 4018c742-1d23-47b9-a787-69bf8847b54a
title: 將外部磁片新增至套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fbfa2ff3d00857fd4e1b92e78f1760c25ce516b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320688"
---
# <a name="adding-foreign-disks-to-a-pack"></a>將外部磁片新增至套件

\[從 Windows 8 和 Windows Server 2012 開始， [虛擬磁碟服務](virtual-disk-service-portal.md) COM 介面會被 [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)取代。\]

最常見的情況是，外部磁片是配置在一部電腦上，並實際移至另一部電腦上的動態磁碟。 不過，屬於線上套件以外套件的任何磁片都會被視為屬於外部磁片套件的外部磁片。

在 [**vds \_ pack \_**](/windows/desktop/api/Vds/ns-vds-vds_pack_prop)架構結構的 **ulFlags** 成員中，有一個外建的 **\_ PKF \_ 外** 旗標已設定的外部套件。 外部套件永遠都是離線的。

下列程式說明如何匯入一或多個外部磁片。

**匯入一或多個外部磁片**

1.  將磁片移至新電腦。
2.  在新電腦上，使用 [**IVdsService：： Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate) 方法來安裝外部磁片。
3.  選取要作為接收外部磁片之目標套件的線上套件。 如果沒有任何線上元件存在，請使用 [**IVdsSwProvider：： CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack) 方法來建立新的空白套件。
4.  使用 [**IVdsPack：： MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks) 方法將磁片匯入至新的動態套件。
5.  使用 [**IVdsSwProvider：： QueryPacks**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-querypacks) 方法來列舉套件，並使用 [**IVdsPack：： GetProperties**](/windows/desktop/api/Vds/nf-vds-ivdspack-getproperties) 來判斷哪個套件現在是線上套件。

如果您建立新的空目標套件，則不會實際將外部磁片遷移至該套件。 相反地，外部套件會標示為 [線上]， (套件的 [ **VDS] \_ PKF \_ 外** 旗標，使套件不再是外部) ，而且會捨棄您所建立的目標套件。

> [!Note]  
> 使用 [**IVdsPack：： AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk) 方法，將未配置的磁片（提供者所宣告的磁片）新增至套件。 未配置的磁片不得為外部。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 VDS](using-vds.md)
</dt> <dt>

[**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate)
</dt> <dt>

[**IVdsSwProvider::CreatePack**](/windows/desktop/api/Vds/nf-vds-ivdsswprovider-createpack)
</dt> <dt>

[**IVdsPack::MigrateDisks**](/windows/desktop/api/Vds/nf-vds-ivdspack-migratedisks)
</dt> <dt>

[**IVdsPack::AddDisk**](/windows/desktop/api/Vds/nf-vds-ivdspack-adddisk)
</dt> </dl>

 

 
