---
description: 登錄是階層式資料庫，其中包含的資料對 Windows 以及在 Windows 上執行的應用程式和服務而言很重要。
ms.assetid: 4ed60563-73d8-4134-8cb2-8388734fb18d
title: 登錄的結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2eb63d49db37bc23eee56bb845c9c5dedf9df7ce4ce610ff8ade500e97cb88e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763489"
---
# <a name="structure-of-the-registry"></a>登錄的結構

登錄是階層式資料庫，其中包含的資料對 Windows 以及在 Windows 上執行的應用程式和服務而言很重要。 資料是以樹狀結構格式進行結構化。 樹狀結構中的每個節點稱為索引 *鍵*。 每個金鑰都可以同時包含子機 *碼和名* 為 *值* 的資料項目。 有時候，索引鍵的存在就是應用程式所需的所有資料。有時候，應用程式會開啟金鑰，並使用與索引鍵相關聯的值。 索引鍵可以有任意數目的值，而值可以是任何形式。 如需詳細資訊，請參閱登錄 [數值型別](registry-value-types.md) 和登錄 [元素大小限制](registry-element-size-limits.md)。

每個金鑰都有一個名稱，其中包含一個或多個可列印字元。 索引鍵名稱不區分大小寫。 索引鍵名稱不能包含反斜線字元 (\\) ，但可以使用任何其他可列印字元。 值名稱和資料可以包含反斜線字元。

每個子機碼的名稱都是唯一的，與階層中緊接在其上的金鑰有關。 索引鍵名稱不會當地語系化為其他語言，雖然值可能為。

下圖是登錄編輯程式所顯示的範例登錄機碼結構。

![[登錄編輯程式] 視窗](images/regtree.png)

**我的電腦** 下的每個樹狀結構都是索引鍵。 **HKEY \_ 本機 \_ 電腦** 金鑰具有下列子機碼：**硬體**、 **SAM**、**安全性**、**軟體** 和 **系統**。 每個金鑰接著都會有子機碼。 例如， **硬體** 金鑰具有子機碼 **DESCRIPTION**、 **DEVICEMAP** 和 **windows.applicationmodel.resources.core.resourcemap**; **DEVICEMAP** 索引鍵有數個子機碼，包含 **影片**。

每個值都包含值名稱及其相關聯的資料（如果有的話）。 **MaxObjectNumber** 和 **VgaCompatible** 是包含 **影片** 子機碼下之資料的值。

登錄樹狀目錄可以是深512層級。 您可以透過單一登入 API 呼叫，一次最多建立32個層級。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 登錄的總覽](/previous-versions/windows/it-pro/windows-server-2003/cc781906(v=ws.10))
</dt> </dl>

 

 
