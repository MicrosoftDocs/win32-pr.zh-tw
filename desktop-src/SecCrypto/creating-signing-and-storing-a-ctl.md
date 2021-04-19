---
description: 建立已簽署的憑證信任清單 (CTL) ，並將其儲存至憑證存放區。
ms.assetid: 82d75d60-2343-413c-ba53-ccee02d1ad41
title: 建立、簽署和儲存 CTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2da66ce5acb882d36451118700178519455a4ded
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973242"
---
# <a name="creating-signing-and-storing-a-ctl"></a>建立、簽署和儲存 CTL

下列程式會建立已簽署的 [*憑證信任清單*](../secgloss/c-gly.md) (CTL) 並將其儲存至 [*憑證存放區*](../secgloss/c-gly.md)。

**建立和簽署 CTL**

1.  建立要儲存在 [*CTL*](../secgloss/c-gly.md)中的專案陣列。 如果是受信任的憑證，這必須是受信任憑證的 SHA1 或 MD5 雜湊。
2.  初始化 [**CTL \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_info) 結構，其中包含剛剛建立之專案的陣列。
3.  將 [**CMSG \_ 簽署的 \_ 編碼 \_ 資訊**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signed_encode_info) 結構初始化。
4.  呼叫 [**CryptMsgEncodeAndSignCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgencodeandsignctl)。 此函式呼叫會傳回 PKCS 7 格式) 的帶正負號編碼 CTL (的指標， \# 其中包含步驟1中建立的專案清單。

**將 CTL 新增至憑證存放區**

1.  取得已簽署且已編碼之 CTL 的指標。
2.  使用 [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)呼叫來開啟目標憑證存放區。
3.  呼叫 [**CertAddEncodedCTLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore)。

 

 
