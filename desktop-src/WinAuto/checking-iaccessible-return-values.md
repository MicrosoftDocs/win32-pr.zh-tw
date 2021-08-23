---
title: 檢查 IAccessible 傳回值
description: 用戶端開發人員不應該相依元件物件模型 (COM) 宏成功，而且無法測試 IAccessible 傳回值，因為 S 以外的值 \_ 會被視為成功。
ms.assetid: 0def0349-178b-4be5-aa1d-6602dc015981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1df43a316898ceeb751b114251ca8fbc91a8fc5360558a3929bcc3ecc47cce1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759628"
---
# <a name="checking-iaccessible-return-values"></a>檢查 IAccessible 傳回值

用戶端開發人員不應該相依元件物件模型 (COM) 宏 [**成功**](/windows/desktop/api/winerror/nf-winerror-succeeded) ，而且 [**無法**](/windows/desktop/api/winerror/nf-winerror-failed) 測試 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 傳回值，因為 S 以外的值 \_ 會被視為成功。 例如，方法可以傳回 \_ FALSE，它會被 **成功** 的宏視為成功，但仍會在輸出參數中收到 **Null** 指標。

用戶端開發人員必須預防某些伺服器傳回錯誤碼以外的錯誤代碼，而不是記錄的值。 為了安全起見，您必須確定所有輸出參數都包含有效的資訊並符合下列準則：

-   所有指標皆為非 **Null**。
-   任何 [變異](/windows/win32/api/oaidl/ns-oaidl-variant)結構的 **vt** 成員都不等於 vt \_ 空白。

 

 