---
description: 進程的虛擬位址空間是一組可用的虛擬記憶體位址。 每個進程的位址空間都是私用的，除非共用，否則無法由其他進程存取。
ms.assetid: 747f9f53-a595-4f4b-8b81-3123d59edb2f
title: '虛擬位址空間 (記憶體管理) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6584d0404799e6b0e5ab343c7d8b39d7f8d741a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943579"
---
# <a name="virtual-address-space-memory-management"></a>虛擬位址空間 (記憶體管理) 

進程的虛擬位址空間是一組可用的虛擬記憶體位址。 每個進程的位址空間都是私用的，除非共用，否則無法由其他進程存取。

虛擬位址不代表物件在記憶體中的實際實體位置;相反地，系統會維護每個進程的 *頁面表格* ，這是用來將虛擬位址轉譯成其對應實體位址的內部資料結構。 每次執行緒參考位址時，系統會將虛擬位址轉譯為實體位址。

32位 Windows 的虛擬位址空間的大小為 4 gb (GB) 並分為兩個磁碟分割：一個供進程使用，另一個則保留供系統使用。 如需64位 Windows 中虛擬位址空間的詳細資訊，請參閱 [64 位 windows 中的虛擬位址空間](../winprog64/virtual-address-space.md)。

如需虛擬記憶體的詳細資訊，請參閱下列主題：

-   [虛擬位址空間和實體儲存體](virtual-address-space-and-physical-storage.md)
-   [工作集](working-set.md)
-   [頁面狀態](page-state.md)
-   [配置的記憶體範圍](scope-of-allocated-memory.md)
-   [資料執行防止](data-execution-prevention.md)
-   [記憶體保護](memory-protection.md)
-   [Windows 版本的記憶體限制](memory-limits-for-windows-releases.md)

## <a name="default-virtual-address-space-for-32-bit-windows"></a>32位 Windows 的預設虛擬位址空間

下表顯示每個資料分割的預設記憶體範圍。



| 記憶體範圍                             | 使用方式                |
|------------------------------------------|----------------------|
| 低 2GB (0x00000000 至 0x7FFFFFFF)   | 由進程使用。 |
| 高 2GB (0x80000000 到 0xFFFFFFFF)  | 供系統使用。  |



 

## <a name="virtual-address-space-for-32-bit-windows-with-4gt"></a>32位 Windows 與4GT 的虛擬位址空間

如果已啟用 [4 gb 調整](4-gigabyte-tuning.md) (4gt) ，則每個分割區的記憶體範圍如下所示。



| 記憶體範圍                             | 使用方式                |
|------------------------------------------|----------------------|
| 低 3GB (0x00000000 至 0xBFFFFFFF)   | 由進程使用。 |
| 高 1GB (透過 0xFFFFFFFF) 0xC0000000 | 供系統使用。  |



 

啟用4GT 之後，在其映射標頭中設定 [**圖像 \_ 檔案 \_ 大型 \_ 位址 \_ 感知**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image) 旗標的進程，將可存取超過 2 gb 以上的額外 1 GB 記憶體。

## <a name="adjusting-the-virtual-address-space-for-32-bit-windows"></a>調整32位 Windows 的虛擬位址空間

您可以使用下列命令來設定開機專案選項，將可供進程使用的磁碟分割大小設定為介於 2048 (2 GB) 和 3072 (3 GB) 之間的值：

[BCDEdit/set](/windows-hardware/drivers/devtest/bcdedit--set) **increaseuserva** *mb*

在設定開機專案選項之後，每個分割區的記憶體範圍如下所示。



| 記憶體範圍                            | 使用方式                |
|-----------------------------------------|----------------------|
| 低 (0x00000000 至 *mb*)     | 由進程使用。 |
| 高 (*mb*+ 1 到 0xffffffff)  | 供系統使用。  |



 

**Windows Server 2003：** 將 boot.ini 中的 **/USERVA** 參數設定為介於2048到3072之間的值。

 

 
