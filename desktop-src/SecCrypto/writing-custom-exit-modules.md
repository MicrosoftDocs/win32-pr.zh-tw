---
description: 自訂結束模組必須執行由伺服器引擎呼叫的 ICertExit 介面。
ms.assetid: 509e7945-b656-4c4c-b5eb-45fbe80377c7
title: 撰寫自訂結束模組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81798996059e878ef11dbcdf290298094d0849cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996908"
---
# <a name="writing-custom-exit-modules"></a>撰寫自訂結束模組

自訂結束模組必須執行由伺服器引擎呼叫的 [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) 介面。 載入結束模組時，伺服器引擎會呼叫 [**ICertExit：： Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize) 方法。 它可讓 exit 模組執行初始化，並傳回值，通知伺服器引擎其需要通知的事件種類。 當伺服器引擎要求時， [**ICertExit：： GetDescription**](/windows/desktop/api/Certexit/nf-certexit-icertexit-getdescription) 方法必須傳回描述字串。 伺服器引擎會呼叫 [**ICertExit：： notify**](/windows/desktop/api/Certexit/nf-certexit-icertexit-notify) 方法，以通知結束模組事件已發生。

結束模組可以呼叫 [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) 介面，此介面支援許多與 [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) 介面相同的方法，但 [**SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) 和 [**SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) 方法除外。

如需移除現有的結束模組，以及安裝新的結束模組的相關資訊，請參閱說明中的結束模組自訂主題。

 

 



