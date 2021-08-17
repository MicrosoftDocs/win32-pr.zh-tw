---
description: 捨棄 \_ IO \_ 要求結構會開始通訊協定控制資訊結構。
ms.assetid: 80fd7c6e-e768-42db-8302-29e92c9552f0
title: 'SCARD_IO_REQUEST 結構 (Winsmcrd .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SCARD_IO_REQUEST
api_type:
- HeaderDef
api_location:
- Winsmcrd.h
ms.openlocfilehash: 9a377643e794b679be593bb99b8750698c92dd3aa8abacd79bfdb1c478c9c7b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918884"
---
# <a name="scard_io_request-structure"></a>捨棄 \_ IO \_ 要求結構

**捨棄 \_ IO \_ 要求** 結構會開始通訊協定控制資訊結構。 任何通訊協定特定的資訊，然後緊接在此結構後面。 整個結構的長度必須與基礎硬體架構的文字大小一致。 例如，在 Win32 中，任何 PCI 資訊的長度都必須是四個位元組的倍數，如此才會在32位界限上對齊。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD dwProtocol;
  DWORD cbPciLength;
} SCARD_IO_REQUEST;
```



## <a name="members"></a>成員

<dl> <dt>

**dwProtocol**
</dt> <dd>

使用中的通訊協定。

</dd> <dt>

**cbPciLength**
</dt> <dd>

**捨棄 \_ IO \_ 要求** 結構的長度（以位元組為單位），加上下列任何 PCI 特定資訊。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Winsmcrd。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SCardTransmit**](/windows/desktop/api/Winscard/nf-winscard-scardtransmit)
</dt> </dl>

 

 




