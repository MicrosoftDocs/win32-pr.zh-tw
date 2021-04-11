---
title: 關於 EAP 和 EAPHost 關聯性
description: 描述可延伸驗證通訊協定 (EAP) 和可延伸的驗證通訊協定主機之間的關聯性。
ms.assetid: 7f585fc6-71ed-4a64-88a7-6acb1550e825
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13c888a6e21992b95ea10f83175c5766246b7aaf
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104196471"
---
# <a name="learn-about-the-eap-and-eaphost-relationship"></a>瞭解 EAP 和 EAPHost 關聯性

本主題說明可延伸的驗證通訊協定 (EAP) 和可延伸的驗證通訊協定主機之間的關聯性。 如需新的 EAP 方法開發，請參閱可延伸的 [驗證通訊協定主機](../eaphost/portal.md)。

## <a name="eaphost-framework"></a>EAPHost 架構

基於兩個原因，EAPHost 被視為適用于 EAP 的架構。

-   EAPHost 是裝載 EAP 外掛程式的 Windows 基礎結構元件
-   EAPHost 會根據 [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84063)來實行 EAP 通訊協定。 EAP 驗證封裝含根據 [RFC 3748](https://go.microsoft.com/fwlink/p/?linkid=84063)的 eap 通訊協定，以及通訊協定的 eap 方法特定層面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 EAP 和 EAPHost](about-extenstible-authentication-protocol-and-eaphhost.md)
</dt> </dl>

 

 
