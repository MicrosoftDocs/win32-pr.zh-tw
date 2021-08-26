---
description: 將交易式 NTFS (TxF) 和交易式登錄 (TxR) 。 TxF 允許 NTFS 內的交易式檔案系統作業。 TxR 允許交易登錄作業。 使用交易來協調檔案系統和登錄作業。
ms.assetid: 2f601994-db1e-4aac-8db1-9a36c702664b
title: 核心交易管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c446931fff4f119217a5f6e5f1b7ae8cf351cf94966a9da5abc4e4d2e88d787
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897528"
---
# <a name="kernel-transaction-manager"></a>核心交易管理員

## <a name="purpose"></a>目的

核心交易管理員 (KTM) 可讓您開發使用交易的應用程式。 交易引擎本身是在核心內，但是可以針對核心或使用者模式交易，以及在單一主機或分散式主機之間開發交易。

KTM 用來執行交易式 NTFS (TxF) 和交易式登錄 (TxR) 。 TxF 允許 NTFS 檔案系統內的交易式檔案系統作業。 TxR 允許交易登錄作業。 KTM 可讓用戶端應用程式使用交易來協調檔案系統和登錄作業。

若要開發以 TxF 或 TxR 以外的資源來協調交易的應用程式，您必須先開發一個 Win32 交易感知服務，也稱為「資源管理員」。

Managed 和 COM + 應用程式應使用其原生交易管理員。

## <a name="where-applicable"></a>適用時

KTM 可以與裝載于 Windows Vista 或 Windows Server 2008 上的應用程式和資源管理員搭配使用。

## <a name="developer-audience"></a>開發人員對象

KTM API 是設計來供 C 和 c + + 程式設計人員使用。

## <a name="run-time-requirements"></a>執行階段需求求

從 Windows Vista 開始支援 KTM。

## <a name="in-this-section"></a>本節內容



| 主題                                     | 描述                                                                                                       |
|-------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [關於](about-ktm.md)<br/>         | 有關交易的一般資訊，以及 KTM 提供的功能。<br/>                           |
| [參考](ktm-reference.md)<br/> | 適用于 KTM 的函式、資料結構、列舉和其他程式設計項目的檔。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[通用記錄檔系統](/previous-versions/windows/desktop/clfs/common-log-file-system-portal)
</dt> <dt>

[交易式 NTFS (TxF) ](/windows/desktop/FileIO/transactional-ntfs-portal)
</dt> <dt>

[分散式交易協調器](/previous-versions/windows/desktop/ms684146(v=vs.85))
</dt> </dl>

 

