---
description: 交易式 NTFS (TxF) 允許在一筆交易中執行 NTFS 檔案系統磁片區上的檔案作業。
ms.assetid: e8c3ceed-d391-4934-b3f7-12c2123c8c23
title: '交易式 NTFS (TxF) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a5b44a35e4f83c1389d1fc2e6bc3de4f97f5ad203bbdee4750c2fcd26d87f47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119431908"
---
# <a name="transactional-ntfs-txf"></a>交易式 NTFS (TxF) 

\[Microsoft 強烈建議開發人員利用替代方法來達成您的應用程式需求。 針對 TxF 開發的許多案例，都可以透過更簡單且更容易使用的技術來達成。 此外，Microsoft Windows 的未來版本可能不提供 TxF。 如需詳細資訊以及 TxF 的替代方案，請參閱 [使用交易式 NTFS 的替代方案](deprecation-of-txf.md)。\]

## <a name="purpose"></a>目的

交易式 NTFS (TxF) 允許在一筆交易中執行 NTFS 檔案系統磁片區上的檔案作業。 TxF 交易可透過跨失敗保護資料完整性來提高應用程式的可靠性，並大幅減少錯誤處理常式代碼的數量，以簡化應用程式開發。

TxF 使用 [核心交易管理員](/windows/desktop/Ktm/kernel-transaction-manager-portal) 所提供的交易架構 (KTM) 。 這可讓 TxF 檔案作業成為牽涉到其他資料來源之交易的一部分，例如 SQL Server 和交易登錄 (TxR) 。

## <a name="where-applicable"></a>適用時

應用程式可以使用 TxF 來保存由於未預期的錯誤狀況所造成之資料的完整性，並藉由在進行變更時隔離您的變更，協助解決並行檔案系統使用者案例。

## <a name="developer-audience"></a>開發人員對象

使用 TxF 之前，您應該具備使用 KTM 或 [分散式交易協調器 (DTC) ](/previous-versions/windows/desktop/ms684146(v=vs.85))之交易的實用知識。

## <a name="run-time-requirements"></a>執行階段需求求

從 Windows Vista 開始提供 TxF。

## <a name="in-this-section"></a>本節內容



| 主題                                                    | 描述                                                                                                |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [關於](about-transactional-ntfs.md)<br/>         | 交易式 NTFS 的一般資訊。<br/>                                                   |
| [參考](transactional-ntfs-reference.md)<br/> | 函數、資料結構、列舉和其他程式設計項目的檔。<br/> |



 

 

