---
title: 搜尋安全性的影響
description: 安全性是執行搜尋、列舉容器或讀取屬性時的隱含篩選。
ms.assetid: 4a027069-8c3d-4a95-a04b-c9c59200a9ed
ms.tgt_platform: multiple
keywords:
- 搜尋 Active Directory 的安全性效果
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 429150489f2ab4d00015744beff72ee2b90b0399afd3d43f9263d39cadbaecd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191618"
---
# <a name="effects-of-security-on-searching"></a>搜尋安全性的影響

安全性是執行搜尋、列舉容器或讀取屬性時的隱含篩選。

即使您沒有讀取物件之屬性的存取權，ADSI 也可以傳回沒有 \_ 這類 \_ 屬性或沒有 \_ 這類 \_ 物件錯誤。

例如，呼叫端可能會列舉容器中的子物件，因為呼叫端在容器上具有清單 \_ 內容許可權。 但是，如果呼叫端沒有子物件的讀取權限，則相同的呼叫端可能無法存取列舉物件。 在此情況下， \_ \_ 即使呼叫端已成功列舉物件，子物件的查詢也可能不會傳回此物件。

如果呼叫端沒有足夠的許可權，可能會傳回下列傳回碼：

E \_ ADS \_ 不正確 \_ 網域 \_ 物件

\_ \_ \_ 不支援 E ADS \_ 屬性

\_ \_ \_ \_ 找不到電子 ADS 屬性

 

 




