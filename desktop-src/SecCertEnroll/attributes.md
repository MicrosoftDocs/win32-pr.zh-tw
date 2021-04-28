---
description: 屬性 (憑證註冊 API) -您可以將屬性新增至憑證要求，以提供憑證授權單位單位 (CA) 以及在建立和發行憑證時可使用的額外資訊。
ms.assetid: 6116e61e-3ec5-4992-90ab-e3c7ced291b6
title: 憑證註冊 API)  (屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 93414156c7fa6e46fe80995d8d01eadc28796ec2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118426"
---
# <a name="attributes-certificate-enrollment-api"></a>憑證註冊 API)  (屬性

您可以將屬性新增至憑證要求，以提供憑證授權單位單位 (CA) 以及可在建立和發行憑證時使用的其他資訊。 每個屬性都是 [*可辨別編碼規則*](/windows/desktop/SecGloss/d-gly) (DER) 編碼 [*抽象語法標記法 (一)*](/windows/desktop/SecGloss/a-gly) (asn.1) 結構，其中包含 (OID) 和零或多個值的物件識別碼。 您可以使用憑證註冊 API 隨附的介面來定義屬性。 下列主題會更詳細地討論屬性：

-   [支援的屬性](supported-attributes.md)
-   [屬性架構](attribute-architecture.md)
-   [PKCS \# 7 屬性](pkcs--7-attributes.md)
-   [PKCS \# 10 屬性](pkcs--10-attributes.md)
-   [CMC 屬性](cmc-attributes.md)

 

 
