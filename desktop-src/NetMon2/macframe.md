---
description: MACFRAME 結構是最常見初始通訊協定的聯集。
ms.assetid: ec7e3a54-a47f-4390-a137-9574c63c9a11
title: 'MACFRAME 聯集 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MACFRAME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: dcff7294d2800e797b43b3a05bd25c35418c6fb466c95130b97be73f25040d3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364706"
---
# <a name="macframe-union"></a>MACFRAME 聯集

**MACFRAME** 結構是最常見初始通訊協定的聯集。

## <a name="syntax"></a>語法


```C++
typedef union {
  LPBYTE      MacHeader;
  LPETHERNET  Ethernet;
  LPTOKENRING Tokenring;
  LPFDDI      Fddi;
} MACFRAME, *LPMACFRAME;
```



## <a name="members"></a>成員

<dl> <dt>

**MacHeader**
</dt> <dd>

框架的泛型指標。

</dd> <dt>

**乙太網路**
</dt> <dd>

框架的乙太網路指標。

</dd> <dt>

**Tokenring**
</dt> <dd>

框架的 Token 環形指標。

</dd> <dt>

**Fddi**
</dt> <dd>

畫面格的 FDDI 指標。

</dd> </dl>

## <a name="remarks"></a>備註

此結構最常用來做為重迭。 若要讓第一個通訊協定的屬性可供存取，請將框架轉換成與通訊協定相同的類型。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



 

 




