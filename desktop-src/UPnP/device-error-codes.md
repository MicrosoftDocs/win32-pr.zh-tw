---
title: 裝置錯誤碼
description: InvokeAction 和 QueryStateVariable 方法會傳回 HRESULT 值，這些值可能指出裝置錯誤 (也就是從 UPnP 認證的裝置) 收到的錯誤。
ms.assetid: 4b18a5d4-f6e8-4670-93dd-ecd012940000
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfcd92d79897318ae6e45fac918dce6af2fe647b
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104463857"
---
# <a name="device-error-codes"></a>裝置錯誤碼

[**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction)和 [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable)方法會傳回 **HRESULT** 值，這些值可能指出裝置錯誤 (也就是從 UPnP 認證的裝置) 收到的錯誤。 如果從裝置收到錯誤，則 ([**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) 或) [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) 的方法會傳回以裝置錯誤碼為基礎的 **HRESULT** 值，如本主題中所述。 因為轉換會套用至裝置錯誤碼以產生 **HRESULT** 值，所以您無法直接從 **HRESULT** 值讀取裝置錯誤碼。

## <a name="conversion-of-a-device-error-code-to-an-hresult"></a>將裝置錯誤碼轉換成 HRESULT

有標準和非標準裝置錯誤碼。 標準程式碼在所有 UPnP 認證的裝置上具有相同的意義，而且其值小於600。 非標準的代碼是廠商專屬的，其值範圍從600到899。

裝置錯誤碼是否為標準，會決定 **HRESULT** 值的產生方式：

-   標準裝置錯誤碼對應至 **HRESULT** 值。

<!-- -->

-   非標準的裝置錯誤碼會藉由套用公式內嵌于 **HRESULT** 值。

這兩個程式都可以反轉，以判斷來自特定 **HRESULT** 值的裝置錯誤碼。

## <a name="deriving-a-device-error-code-from-an-hresult-value"></a>從 HRESULT 值衍生裝置錯誤碼

如果 **HRESULT** 值大於或等於 **upnp \_ e \_ 動作 \_ 特定 \_ 基底** (0x80040300) 且小於或等於 **upnp \_ e \_ 動作 \_ 特定的 \_ 最大** (0x8004042B) ，則裝置錯誤碼並非標準用法，請使用下一節中的公式來判斷錯誤碼。 否則，裝置錯誤碼是標準的-使用對應中的 [標準裝置錯誤碼] 區段的表格，提供從 **HRESULT** 值到裝置錯誤碼的對應。

如需呼叫 [**IUPnPService：： InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction)之後之錯誤的文字描述，請將 *pvarRetVal* 參數設定為空陣列。 傳回時，如果發生錯誤，此參數將包含錯誤的文字描述。

### <a name="formula-for-nonstandard-device-error-codes"></a>非標準裝置錯誤碼的公式

如果 **upnp \_ e \_ 動作 \_ 特定的 \_ 基底** ≤ **HRESULT** ≤**upnp \_ e \_ 動作特定的 \_ \_ 最大值**，請使用下列公式。

裝置錯誤碼 = (**HRESULT**  -  **UPNP \_ E \_ 動作特定的 \_ \_ 基底**) +**錯誤 \_ 動作特定的 \_ \_ 基底**

替代實際數值，方程式是：裝置錯誤碼 = (**HRESULT** -0x80040300) + 0x0258

### <a name="mapping-for-standard-device-error-codes"></a>標準裝置的對應錯誤代碼

如果 **HRESULT**  <  **UPNP \_ E \_ 動作 \_ 特定的 \_ 基底**，請使用下列對應。



| HRESULT 值                    | 裝置錯誤碼                | 實際值 |
|----------------------------------|----------------------------------|--------------|
| UPNP \_ E \_ 不正確 \_ 動作         | 錯誤 \_ 不正確 \_ 動作           | 401          |
| UPNP \_ E \_ 不正確 \_ 引數      | 錯誤 \_ 不正確 \_ ARG              | 402          |
| UPNP \_ E \_ 不 \_ \_ 同步           | 錯誤 \_ 不正確 \_ 序號 \_ | 403          |
| UPNP \_ E \_ 不正確 \_ 變數       | 錯誤 \_ 不正確 \_ 變數         | 404          |
| UPNP \_ 電子 \_ 動作 \_ 要求 \_ 失敗 | 錯誤 \_ 裝置 \_ 內部 \_ 錯誤   | 501          |



 

## <a name="more-information"></a>相關資訊

[UPnP 裝置架構版本 1.0](https://openconnectivity.org/resources/documents.asp)中指定了裝置錯誤碼。 本主題所述的常數定義于檔案的 Upnp 和 Upnp 中。

 

 




