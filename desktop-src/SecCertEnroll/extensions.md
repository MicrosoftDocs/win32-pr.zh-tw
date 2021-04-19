---
description: X.509 第3版憑證格式可識別多個可新增至憑證的延伸模組。
ms.assetid: f2a6854d-1831-489f-adf6-31a0b26511e3
title: 憑證註冊 API) 的延伸模組 (
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extensions
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5478b8edeff3524ada760cc5680f5c9dca359e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978265"
---
# <a name="extensions-certificate-enrollment-api"></a>憑證註冊 API) 的延伸模組 (

X.509 第3版憑證格式可識別多個可新增至憑證的延伸模組。 延伸模組提供有關金鑰使用方式、憑證原則和條件約束、替代名稱表單等的增強資訊。 您可以使用 [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) 介面來定義延伸模組值。 您可以使用衍生自 **IX509Extension** 的預先定義介面來建立許多常見的擴充功能。 擴充功能的集合會在要求屬性中包含集合，藉此新增至憑證要求。 如需詳細資訊，請參閱下列主題：

-   [支援的延伸模組](supported-extensions.md)
-   [PKCS \# 10 擴充功能](pkcs--10-extensions.md)
-   [CMC 延伸模組](cmc-extensions.md)

 

 



