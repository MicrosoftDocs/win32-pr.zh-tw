---
description: WindowsServer 2008 R2 和 Windows 7 對磁碟區陰影複製服務引進了下列變更。
ms.assetid: 1287f175-29e4-40be-804b-d78542e76efc
title: 新功能： Windows Server 2008 R2 中的 VSS & Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eeaaf42a82e13c5766ee3cfa6ba9fe73a36a783824497482ac97fc20d058a51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118121524"
---
# <a name="whats-new-vss-in-windows-server-2008-r2--windows-7"></a>新功能： Windows Server 2008 R2 中的 VSS & Windows 7

WindowsServer 2008 R2 和 Windows 7 對磁碟區陰影複製服務引進了下列變更。

## <a name="new-vss-interfaces"></a>新的 VSS 介面

<dl>

[**IVssBackupComponentsEx3**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex3)  
[**IVssComponentEx2**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex2)  
[**IVssCreateExpressWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreateexpresswritermetadata)  
[**IVssExpressWriter**](/windows/desktop/api/VsWriter/nl-vswriter-ivssexpresswriter)  
</dl>

## <a name="new-vss-classes"></a>新的 VSS 類別

<dl>

[**CVssWriterEx2**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriterex2)  
</dl>

## <a name="new-vss-enumerations"></a>新的 VSS 列舉

<dl>

[**VSS \_ 修復 \_ 選項**](/windows/desktop/api/Vss/ne-vss-vss_recovery_options)  
</dl>

## <a name="new-vss-functions"></a>新的 VSS 函式

<dl>

[**CreateVssExpressWriter**](/windows/desktop/api/VsWriter/nf-vswriter-createvssexpresswriter)  
</dl>

## <a name="existing-vss-interface-modifications"></a>現有的 VSS 介面修改

<dl>

[**IVssHardwareSnapshotProviderEx**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex) 介面<dl> 新增的方法： [ **ResyncLuns**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotproviderex-resyncluns)  
</dl> </dd> </dl>

## <a name="vss-event-tracing-and-logging"></a>VSS 事件追蹤和記錄

從 Windows Server 2008 R2 和 Windows 7 開始，您可以使用 VssTrace 工具、Logman 工具或 tracelog.exe 工具來收集 VSS 基礎結構的追蹤資訊。 如需詳細資訊，請參閱搭配 [使用追蹤工具和 VSS](using-tracing-tools-with-vss.md)。

## <a name="lun-resynchronization"></a>LUN 重新同步處理

在 Windows Server 2008 R2 和 Windows 7 中，VSS 要求者可以使用名為 LUN 重新同步 (LUN resynchronization 或 LUN resync) 的硬體陰影複製提供者功能。 這是一種快速復原配置，可讓應用程式系統管理員將資料從陰影複製還原到原始的邏輯單元編號 (LUN) 或新的 LUN。 陰影複製可以是完整再製或差異陰影複製。 不論是哪一種情況，在重新同步作業結束時，目的地 LUN 的內容都會與陰影複製 LUN 相同。 在重新同步作業期間，陣列會執行從陰影複製到目的地 LUN 的區塊層級複製。 如需詳細資訊，請參閱下列：

-   [LUN 重新同步-Server 2008 R2 中的快速復原案例](https://blogs.technet.com/filecab/archive/2009/04/11/lun-resync-a-fast-recovery-scenario-in-server-2008-r2.aspx)
-   [磁碟區陰影複製服務](/windows-server/storage/file-server/volume-shadow-copy-service)中的「如何使用陰影複製」
-   [常見的 LUN 重新同步問題](https://blogs.msdn.com/gregd/archive/2009/07/27/common-lun-resync-gotchas.aspx)

## <a name="express-writers"></a>快速寫入器

在 Windows Server 2008 R2 和 Windows 7 中，VSS express 介面可讓應用程式註冊其資料檔案的位置，而不需要執行 VSS 寫入器。 如需詳細資訊，請參閱 [磁碟區陰影複製服務 (VSS) Express 寫入](https://blogs.technet.com/filecab/archive/2009/06/17/volume-shadow-copy-service-vss-express-writers.aspx)器。

## <a name="new-vss-writers"></a>新的 VSS 寫入器

WindowsServer 2008 R2 和 Windows 7 引進下列 VSS 寫入器：

-   效能計數器寫入器
-   工作排程器寫入器
-   VSS 中繼資料存放區寫入器

這些新的寫入器記載于 [內建的 VSS 寫入](in-box-vss-writers.md)器中。

 

 
