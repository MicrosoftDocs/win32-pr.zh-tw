---
description: 使用 VDS
ms.assetid: aa4be499-625d-4dbd-828c-4a55ff2dba2c
title: 使用 VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6406e938a8fb49314511047bb038ec94a5af9151f5c077ad1fb14984e74474f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125864"
---
# <a name="using-vds"></a>使用 VDS

\[從 Windows 8 和 Windows Server 2012 開始， [Windows 儲存體管理 API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)會取代[虛擬磁碟服務](virtual-disk-service-portal.md)COM 介面。\]

VDS 為腳本和 GUI 開發提供了一個介面，可以簡化管理一組異類儲存體系統的 Windows server 系統管理員所執行的活動，並在一段時間內跨不同的硬體設定遷移資料。 如果您不熟悉在 VDS 開發中使用的物件，請參閱 [Vds 物件模型](vds-object-model.md)。

開始之前的幾個要點：

-   雖然 VDS 包含軟體提供者，但您必須個別購買硬體提供者和相關聯的硬體，才能利用硬體提供者作業。 如需安裝指示，請參閱硬體製造商所提供的檔。
-   某些作業需要 NTFS 格式的磁片區。 例如，當您在現有的目錄上掛接磁片區時，包含該目錄的磁片區必須格式化為 NTFS。 其他檔案系統不支援此操作。 如需有關需要 NTFS 之作業的詳細資訊，請參閱 [VDS 參考](vds-reference.md)中的每個方法頁面。

## <a name="programming-languages"></a>程式語言：

使用適用于使用 COM 進行開發的任何程式設計語言，例如 C 語言或 c + +。

## <a name="security"></a>安全性

Windows預設會啟用防火牆。 這可能會導致可遠端執行的回呼介面（例如 [**IVdsAdviseSink**](/windows/desktop/api/Vds/nn-vds-ivdsadvisesink)）的驗證失敗。 如果用戶端或伺服器上已啟用 Windows 防火牆，您必須將遠端磁片區管理新增至 Windows 防火牆的 [**例外**] 索引標籤。

**Windows Server 2003：** 在 Windows Server 2003 （含 service pack 2） (SP2) 和 Windows Server 2003 Service pack 1 (SP1) 中，如果在用戶端或伺服器上啟用 Windows 防火牆，且伺服器設定為使用 NTLM 驗證，則您必須將下列設定新增至適用電腦 Windows 防火牆的 [**例外**] 索引標籤中。

| 電腦                 | 例外狀況設定                                                                 |
|--------------------------|-------------------------------------------------------------------------------------|
|  (本機) 的用戶端電腦  | Dmremote.exe<br/> Mmc.exe<br/> Vdsldr.exe<br/> TCP 135<br/> |
|  (遠端) 的伺服器電腦 | Dmadmin.exe<br/> Vds.exe<br/> TCP 135<br/>                        |



 

請注意，在 Windows Server 2003 SP1 之前，預設不會啟用 Windows 防火牆。

使用 VDS 的應用程式必須在 Backup 操作員或 Administrators 群組帳戶下執行。 如果沒有適當的許可權，應用程式可以建立服務載入器物件，但物件不會載入 VDS。 相反地，它會傳回錯誤，指出拒絕存取 VDS。

如果網路使用 NTLM 驗證，用戶端電腦應該允許匿名存取。 在此情況下，如果用戶端電腦正在執行 Windows Server 作業系統，則預設會啟用匿名存取。 如果正在執行 Windows 用戶端作業系統，則必須使用 Dcomcnfg.exe 來啟用匿名存取。

## <a name="configuration-and-query-operations"></a>設定和查詢作業

設定和查詢作業的範圍是最相關的電腦、提供者、子系統或套件。 查詢只會跨越一個提供者或一個層級的系結階層。 若要建立完整的視圖，呼叫端必須在每個層級之間進行查詢。 下列清單包含範例：

-   若要查看電腦上的所有磁片，呼叫者必須針對那些提供者所宣告的磁片，在所有軟體提供者上進行查詢。
-   為了判斷哪些磁片有助於軟體堆疊磁片區，呼叫端會先判斷參與的 plex，然後查詢每個叢的磁片區。
-   若要查看所有連接到指定子系統的磁片磁碟機，呼叫端必須查詢子系統。
-   若要查看由指定子系統公開的所有 Lun，呼叫端必須查詢子系統。
-   若要查看 SAN 或叢集上的所有存放裝置，呼叫端必須查詢每部電腦的所有硬體提供者、查詢所有子系統的每個提供者，然後查詢每個子系統。

雖然每個個別查詢都不會傳回重複專案，但是跨電腦或跨提供者的重複查詢可能會累積重複專案。 呼叫端必須執行任何篩選。 另外也請注意，SAN 管理應用程式可以使用 Active Directory 或存放庫來保存設定資訊;可能不需要查詢每部電腦。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[虛擬磁碟服務](virtual-disk-service-portal.md)
</dt> <dt>

[VDS 物件模型](vds-object-model.md)
</dt> <dt>

[VDS 參考](vds-reference.md)
</dt> </dl>

 

