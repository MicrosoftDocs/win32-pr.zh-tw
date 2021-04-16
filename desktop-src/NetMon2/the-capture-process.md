---
description: 這四個 NPP 介面的捕獲程式都相同。
ms.assetid: f778aba5-8f66-4fc9-830b-f830c364da56
title: 捕獲進程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0ca1987266b7e042713f1d1c292cf63d5e3ccf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570988"
---
# <a name="the-capture-process"></a>捕獲進程

這四個 NPP 介面的捕獲程式都相同。 在每個案例中，處理常式包括：

-   取得要使用的 NPP 介面物件
-   連接到網路
-   啟動並停止 [*捕獲*](c.md)
-   中斷與網路的連線

> [!Note]  
> 當您取得所需的介面物件時，請確定您只呼叫該介面中包含的方法。 下圖顯示每個介面都提供類似的方法來捕捉網路資料。 如果您使用一個介面連接到網路，然後嘗試使用其他介面中的方法來執行捕捉，則會傳回錯誤。

 

下圖顯示兩個您可以執行捕捉的不同方式。 第一個圖例顯示如何執行一或多個連續的捕獲，讓您可以建立任意數目的獨立捕獲。

![連續捕捉](images/capt1.png)

如上所示，在連線到網路之後，您可以視需要多次啟動和停止 capture，啟動新的捕獲，並在每次重新開機捕獲時產生新的統計資料。 例如，針對使用 [**IDelaydC**](idelaydc.md) 介面的延遲捕捉，每次您重新開機捕獲時，就會建立新的 [*capture*](c.md) 檔。

不過，也請注意，每次您重新開機 capture 程式時，都必須呼叫適當的 configure 方法來重新設定連接。 針對開始捕獲的初始呼叫，連接是透過連接到網路的呼叫來設定。

第二個圖例顯示如何藉由暫停和重新開機來執行單一捕獲。

![藉由暫停和重新開機來進行單一捕獲](images/capt2.png)

在此情況下，您可以依需要暫停和重新開機 capture。 使用這個方法時，您可以執行資料 (的捕獲，並將其相關的統計資料) 記錄為單一捕獲。 例如，若要使用 [**IDelaydC**](idelaydc.md) 介面執行延遲的捕獲，所有捕獲的網路資訊都會儲存在單一的 [*捕獲*](c.md)檔案中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CreateNPPInterface**](createnppinterface.md)
</dt> <dt>

[**IDelaydC：： Configure**](idelaydc-configure.md)
</dt> <dt>

[**IDelaydC：： Connect**](idelaydc-connect.md)
</dt> <dt>

[**IDelaydC：:D isconnect**](idelaydc-disconnect.md)
</dt> <dt>

[**IDelaydC：:P ause**](idelaydc-pause.md)
</dt> <dt>

[**IDelaydC：： Resume**](idelaydc-resume.md)
</dt> <dt>

[**IDelaydC：： Start**](idelaydc-start.md)
</dt> <dt>

[**IDelaydC：： Stop**](idelaydc-stop.md)
</dt> <dt>

[**IESP：： Configure**](iesp-configure.md)
</dt> <dt>

[**IESP：： Connect**](iesp-connect.md)
</dt> <dt>

[**IESP：:D isconnect**](iesp-disconnect.md)
</dt> <dt>

[**IESP：:P ause**](iesp-pause.md)
</dt> <dt>

[**IESP：： Resume**](iesp-resume.md)
</dt> <dt>

[**IESP：： Start**](iesp-start.md)
</dt> <dt>

[**IESP：： Stop**](iesp-stop.md)
</dt> <dt>

[**IRTC：： Configure**](irtc-configure.md)
</dt> <dt>

[**IRTC：： Connect**](irtc-connect.md)
</dt> <dt>

[**IRTC：:D isconnect**](irtc-disconnect.md)
</dt> <dt>

[**IRTC：:P ause**](irtc-pause.md)
</dt> <dt>

[**IRTC：： Resume**](irtc-resume.md)
</dt> <dt>

[**IRTC：： Start**](irtc-start.md)
</dt> <dt>

[**IRTC：： Stop**](irtc-stop.md)
</dt> <dt>

[**IStats：： Configure**](istats-configure.md)
</dt> <dt>

[**IStats：： Connect**](istats-connect.md)
</dt> <dt>

[**IStats：:D isconnect**](istats-disconnect.md)
</dt> <dt>

[**IStats：:P ause**](istats-pause.md)
</dt> <dt>

[**IStats：： Resume**](istats-resume.md)
</dt> <dt>

[**IStats：： Start**](istats-start.md)
</dt> <dt>

[**IStats：： Stop**](istats-stop.md)
</dt> </dl>

 

 



