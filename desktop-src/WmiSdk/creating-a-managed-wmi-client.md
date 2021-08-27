---
description: WMI 目前不支援 WMI 上的 managed 程式碼，但在 MI 上則支援。
ms.assetid: ED6EF216-7FF7-45F2-9FDD-3A73D5F65F9B
ms.tgt_platform: multiple
title: 建立受控 WMI 用戶端
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6f28b01cb3b4506e0b47332cc3336af95dd641e78c7716f33b8e62b162081bdd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071518"
---
# <a name="creating-a-managed-wmi-client"></a>建立受控 WMI 用戶端

目前的 WMI 版本包含管理命名空間，此命名空間會公開與 WMI 互動的許多 API。 但是，不建議使用此命名空間。

如果您想要建立受控 WMI 用戶端，建議您使用 Windows 管理基礎結構 (MI) 。 MI 是新一代的 WMI 版本，包含對 managed 程式碼的完整支援。 如需詳細資訊，請參閱 [如何執行受管理的 MI 用戶端](/previous-versions/windows/desktop/wmi_v2/how-to-implement-a-managed-mi-client)。

 

 
