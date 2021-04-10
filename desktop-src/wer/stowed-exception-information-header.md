---
title: STOWED_EXCEPTION_INFORMATION_HEADER 結構
description: 包含識別父結構的資訊。
ms.assetid: 0BC1FDAA-C750-4DEC-AF6A-B2CB3240B67C
keywords:
- STOWED_EXCEPTION_INFORMATION_HEADER 結構 Windows 錯誤報告
- PSTOWED_EXCEPTION_INFORMATION_HEADER 結構指標 Windows 錯誤報告
topic_type:
- apiref
api_name:
- STOWED_EXCEPTION_INFORMATION_HEADER
api_location:
- none
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 101bb1fb1555c829622a42c17fdfb01488c57636
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025404"
---
# <a name="stowed_exception_information_header-structure"></a>STOWED \_ 例外狀況 \_ 資訊 \_ 標頭結構

包含識別父結構的資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _STOWED_EXCEPTION_INFORMATION_HEADER {
  ULONG Size;
  ULONG Signature;
} STOWED_EXCEPTION_INFORMATION_HEADER, *PSTOWED_EXCEPTION_INFORMATION_HEADER;
```



## <a name="members"></a>成員

<dl> <dt>

**大小**
</dt> <dd>

類型： **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

父結構的大小（以位元組為單位）。

</dd> <dt>

**簽名**
</dt> <dd>

類型： **[ **ULONG**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

指定父結構簽章的32位值。



| 值                                                                                                                                                                                                                                                                                                            | 意義                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_INFORMATION_V1_SIGNATURE"></span><span id="stowed_exception_information_v1_signature"></span><dl> <dt>**STOWED \_例外狀況 \_ 資訊 \_ V1 \_ 簽名碼**</dt> <dt>' SE01 '</dt> </dl> | 這個值表示父系是 **STOWED \_ 例外狀況 \_ 資訊 \_ V1** 結構。<br/>                                        |
| <span id="STOWED_EXCEPTION_INFORMATION_V2_SIGNATURE"></span><span id="stowed_exception_information_v2_signature"></span><dl> <dt>**STOWED \_例外狀況 \_ 資訊 \_ V2 \_ 簽名碼**</dt> <dt>' SE02 '</dt> </dl> | 這個值表示父系是 [**STOWED \_ 例外狀況 \_ 資訊 \_ V2**](stowed-exception-information-v2.md) 結構。<br/> |



 

</dd> </dl>

## <a name="remarks"></a>備註

[**STOWED \_例外狀況 \_ 資訊 \_ V2**](stowed-exception-information-v2.md) 和 **STOWED 例外狀況 \_ \_ 資訊 \_ 標頭** 目前未定義于可公開取得的標頭中，因此您必須先在原始程式碼中定義它們，然後才能使用它們。

**STOWED \_ 例外狀況 \_ 資訊 \_ V1** 結構與此結構相同，但不包含 **NestedExceptionType** 和 **NestedException** 成員。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>None</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**STOWED \_ 例外狀況 \_ 資訊 \_ V2**](stowed-exception-information-v2.md)
</dt> </dl>

 

