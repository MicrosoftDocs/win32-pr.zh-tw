---
title: 可延伸的驗證通訊協定主機
description: 瞭解 (EAP) 主機的可延伸驗證通訊協定。 請參閱執行時間需求並查看其他可用的資源。
ms.assetid: caaef367-2952-44fc-ac4c-f0db6387850e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62bd43feec10cfadf4aee071ff5f7fe98da5d579878231b9ba3e86287bf4dbab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117719813"
---
# <a name="extensible-authentication-protocol-host"></a>可延伸的驗證通訊協定主機

## <a name="purpose"></a>目的


EAPHost 是一種 Microsoft Windows 網路元件，提供可延伸的驗證通訊協定 (EAP) 基礎結構，以驗證 "要求者" 通訊協定的執行，例如[802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10))和[點對點](https://go.microsoft.com/fwlink/p/?linkid=83919) (PPP) 。 它也可讓您使用「驗證器」技術進行驗證，例如 Microsoft 網路原則伺服器 (NPS) 。 不同于先前的 資訊存取伺服器 ([RADIUS](/windows/desktop/Nps/ias-about-internet-authentication-service)) ，NPS 支援 (NAP) 的 [網路存取保護](/windows/desktop/NAP/network-access-protection-start-page) 。


EAPHost Api 可讓應用程式使用 EAPHost 服務進行驗證，並提供用於開發一致驗證方法以與 EAPHost 搭配使用的範本。

## <a name="run-time-requirements"></a>執行階段需求求

只有 Windows Vista 和更新版本的作業系統才支援 EAPHost api。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 EAPHost](about-eap-host.md)
</dt> <dt>

[使用 EAPHost](using-eap-host.md)
</dt> <dt>

[EAPHost API 參考](eaphost-api-reference.md)
</dt> </dl>

 

 