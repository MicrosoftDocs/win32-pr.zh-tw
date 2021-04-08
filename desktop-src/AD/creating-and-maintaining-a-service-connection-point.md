---
title: 建立和維護服務連接點
description: 使用 SCP 發佈時，請記住，它必須包含服務實例的最新資料。
ms.assetid: 2350cb65-3439-4a5f-adc5-b71476793247
ms.tgt_platform: multiple
keywords:
- 建立和維護服務連接點 AD
- 服務連接點 AD、建立和維護
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6c4ad02b92fa6567fc3b709e45f2f64ce66318
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023265"
---
# <a name="creating-and-maintaining-a-service-connection-point"></a>建立和維護服務連接點

使用 SCP 發佈時，請記住，它必須包含服務實例的最新資料。 否則，系結至 SCP 的用戶端會取出過期的資料。 建立 SCP 的服務安裝程式會指定 Scp 屬性的初始值。 然後，當服務實例啟動時，它必須找出 SCP 並更新屬性值（如有必要）。 如此一來，用戶端就可以確保最新的資料。

建立 SCP 之後，您的服務安裝程式會執行兩個額外的步驟，讓您的服務更新 SCP：

-   在 SCP 物件的安全描述項中設定 Ace，讓服務在執行時間修改 SCP 屬性。 如需詳細資訊和程式碼範例，請參閱 [啟用服務帳戶以存取 SCP 屬性](enabling-service-account-to-access-scp-properties.md)。
-   在服務主機電腦上的登錄中快取 SCP 的 **objectGUID** 。 服務會抓取快取的 GUID 以系結至 SCP，以驗證並更新其屬性。

服務安裝程式會快取 SCP 的 **objectGUID** ，而不是其 DN。 **ObjectGUID** 永遠不會變更，不論 SCP 是否已移動或重新命名。 如果系統管理員移動或重新命名 SCP，則 DN 可能會變更。 例如，如果您將 SCP 建立為電腦物件的子系，則如果電腦已重新命名或移至不同的網域或組織單位，SCP 的辨別名稱就會變更。

當服務安裝程式建立 SCP 時，它必須讀取新建立之物件的 **objectGUID** ，並在服務主機電腦的登錄中加以快取。 使用 [**IADs：： get \_ GUID**](/windows/desktop/ADSI/iads-property-methods) 方法可取得適用于系結的字串格式的 **objectGUID** 值。 將 GUID 字串快取為下列登錄機碼下的值。

```
HKEY_LOCAL_MACHINE
   vendor name
      product name
```

其中「廠商名稱」和「產品名稱」可識別廠商和產品。

當服務啟動時，會從登錄抓取快取的 GUID 字串，並使用它來系結至 SCP。 服務會讀取重要的 SCP 屬性，並將它們與目前的值進行比較。 如果 SCP 值過期，則服務會更新這些值。 服務可能需要更新的值包括 **關鍵字**、 **serviceBindingInformation**、 **serviceDNSName** 和 **serviceDNSNameType**。

## <a name="examples"></a>範例

-   [腳本範例](script-samples-for-managing-service-connection-points.md)
-   [C/c + +) 範例 (程式碼](code-samples-for-managing-service-connection-points.md)

 

 