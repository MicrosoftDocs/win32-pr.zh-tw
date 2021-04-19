---
description: 定義可同時在802.11 站上啟用的一組802.11 驗證和加密演算法。
ms.assetid: 5fbe23f6-7902-46d4-a1f0-57f045d78662
title: 'DOT11_AUTH_CIPHER_PAIR 結構 (Wlantypes .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_AUTH_CIPHER_PAIR
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: fd1a8ef03d5c5cb897d95b768f8ab48705098d74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975753"
---
# <a name="dot11_auth_cipher_pair-structure"></a>DOT11 \_ AUTH \_ CIPHER \_ 成對結構

**DOT11 \_ AUTH \_ CIPHER \_** 組結構會定義一組802.11 驗證和加密演算法，可在802.11 站上同時啟用。

## <a name="syntax"></a>語法


```C++
typedef struct _DOT11_AUTH_CIPHER_PAIR {
  DOT11_AUTH_ALGORITHM   AuthAlgoId;
  DOT11_CIPHER_ALGORITHM CipherAlgoId;
} DOT11_AUTH_CIPHER_PAIR, *PDOT11_AUTH_CIPHER_PAIR;
```



## <a name="members"></a>成員

<dl> <dt>

**AuthAlgoId**
</dt> <dd>

使用 [**DOT11 \_ AUTH \_ 演算法**](dot11-auth-algorithm.md) 列舉類型的驗證演算法。

</dd> <dt>

**CipherAlgoId**
</dt> <dd>

使用 [**DOT11 \_ cipher \_ 演算法**](dot11-cipher-algorithm.md) 列舉型別的密碼演算法。

</dd> </dl>

## <a name="remarks"></a>備註

DOT11 \_ AUTH \_ CIPHER 的 \_ 結構定義了一種驗證和密碼演算法，可同時為基本服務集 (BSS) 網路連線啟用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista、Windows XP （僅含 SP3） \[ 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                        |
| 可轉散發套件<br/>          | 適用于 Windows XP SP2 的無線區域網路 API<br/>                                                         |
| 標頭<br/>                   | <dl> <dt>Wlantypes (包含 Windot11) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DOT11 \_ AUTH \_ 演算法**](dot11-auth-algorithm.md)
</dt> <dt>

[**DOT11 \_ 密碼 \_ 演算法**](dot11-cipher-algorithm.md)
</dt> </dl>

 

 




