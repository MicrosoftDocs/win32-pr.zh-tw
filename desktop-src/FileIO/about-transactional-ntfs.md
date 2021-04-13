---
description: 交易式 NTFS (TxF) 將交易整合至 NTFS 檔案系統，讓應用程式開發人員和系統管理員可以更輕鬆地處理錯誤並保持資料完整性。
ms.assetid: 52341315-0412-4a87-aca0-9adea7aae62f
title: 關於交易式 NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcf8cd99dfb1ff18ef7da88d3b3c7b0a647417e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318432"
---
# <a name="about-transactional-ntfs"></a>關於交易式 NTFS

\[Microsoft 強烈建議開發人員利用替代方法來達成您的應用程式需求。 針對 TxF 開發的許多案例，都可以透過更簡單且更容易使用的技術來達成。 此外，Microsoft Windows 的未來版本可能不提供 TxF。 如需詳細資訊以及 TxF 的替代方案，請參閱 [使用交易式 NTFS 的替代方案](deprecation-of-txf.md)。\]

交易式 NTFS (TxF) 將交易整合至 NTFS 檔案系統，讓應用程式開發人員和系統管理員可以更輕鬆地處理錯誤並保持資料完整性。

TxF 可以參與 [分散式交易協調器 (DTC) ](/previous-versions/windows/desktop/ms684146(v=vs.85)) 協調的分散式交易，這可讓您針對下列各項使用 TxF：

-   跨多個資料存放區的交易，例如，檔案和 SQL 作業的單一交易
-   跨多部電腦的交易（例如，在多部電腦上進行檔案更新的單一交易）

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                                 | 描述                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [使用交易式 NTFS 的時機](when-to-use-transactional-ntfs.md)<br/>                                       | 使用交易式 NTFS 來維護資料完整性。<br/>                                                                        |
| [部署交易式 NTFS](deploying-transactional-ntfs.md)<br/>                                           | 在交易式 NTFS 中快取控制項。<br/>                                                                                    |
| [如何使用交易式 NTFS](how-to-use-transactional-ntfs.md)<br/>                                         | 管理交易式 NTFS 中的交易式檔案控制代碼。<br/>                                                                   |
| [基本 TxF 概念](txf-basic-concepts.md)<br/>                                                               | 描述交易式 NTFS 中的讀取認可一致性、讀取認可隔離和交易鎖定概念。<br/> |
| [交易式 NTFS 的程式設計考慮](programming-considerations-for-transacted-fileio-.md)<br/> | 描述交易式 NTFS 的各種程式設計考慮。<br/>                                                      |
| [交易式 NTFS 的效能考慮](performance-considerations-for-transactional-ntfs.md)<br/> | 最佳檔案系統交易的建議。<br/>                                                                     |



 

 

