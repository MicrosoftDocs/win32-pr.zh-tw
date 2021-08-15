---
description: 開發 COM + CRM 的設計建議
ms.assetid: dde1b978-6d35-4a75-91fd-69dfcc6c43d2
title: 開發 COM + CRM 的設計建議
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a286b2aa75b266a41b249b29203b16f0441e6276a9de03a25efc622ac2bd3fdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128750"
---
# <a name="design-suggestions-for-developing-a-com-crm"></a>開發 COM + CRM 的設計建議

以下是開發 COM + CRM 的建議步驟：

1.  開始開發之前，請使用 [元件服務] 系統管理工具) 將交易超時設定為零 (。 設定 VTRACE1 登錄旗標 (查看[com + CRM 登錄設定](com--crm-registry-settings.md)) 以查看調試追蹤上的 CRM 警告和錯誤訊息。
2.  判斷您需要使用的介面集、結構化 (變異) 或非結構化。  (請參閱[com + CRM 介面](com--crm-interfaces.md)。 ) 這將取決於您用來開發 CRM 的語言，例如 Microsoft Visual C++ 或 Microsoft Visual Basic。
3.  先開發 CRM 背景工作角色。 判斷記錄檔記錄中所需的資訊。 定義所需的記錄檔記錄類型和其格式。
4.  在 Windows SDK) 中，會在 crm 範例 (中提供 debug crm 補償器的一部分。 當您將 CRM 工作者取代為實際的 CRM 補償器時，可以暫時使用這項功能。
5.  當 CRM 背景工作正常運作時，開發實際的 CRM 補償器，並將 debug CRM 補償器取代為實際的 CRM 補償器。
6.  建議您一開始不需要測試復原案例。 若是如此，請在啟動 crm 伺服器應用程式之前，每次都刪除 CRM 伺服器應用程式的 CRM 記錄檔。

## <a name="considerations"></a>考量

1.  **事先撰寫。** CRM 背景工作元件必須先行寫入;也就是說，它必須撰寫記錄檔記錄，指出它會在實際執行該動作之前執行動作。 此外，此記錄檔記錄必須在寫入後和執行動作之前強制寫入磁片。
2.  **分離。** CRM 不會強制執行隔離。 CRM 設計必須在不同的交易上提供多個用戶端之間的隔離，而且也必須考慮復原之前的案例。
3.  **正在復原。** CRM 工作者必須處理「正在復原」錯誤碼。 如需有關此錯誤碼的詳細資訊，請參閱 [COM + CRM 的疑難排解](troubleshooting-the-com--crm.md) 。
4.  **錯誤處理。** CRM 工作者必須處理交易比預期早中止的情況。 請參閱 [COM + CRM 中的錯誤處理](error-handling-in-the-com--crm.md)一節。
5.  **復原時間。** CRM 補償器應設計為可快速執行復原，讓該 CRM 伺服器應用程式的新工作不需要等待。
6.  **等冪.** CRM 補償器可能會再次收到相同的記錄檔記錄，以復原或重做已復原或重做的動作。 CRM 補償器可能執行的動作必須具有等冪性，這通常表示應該忽略從這些動作傳回的錯誤碼。
7.  **復原的初始。** 當 CRM 伺服器應用程式啟動時，就會執行 CRM 伺服器應用程式的復原。 但是，CRM 伺服器應用程式並不會自動啟動。 應用程式開發人員應該考慮啟動和復原的起始方式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 補償 Resource Manager 概念](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



