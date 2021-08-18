---
description: 包含智慧卡密碼編譯服務提供者 (CSP) 的相關資訊。
ms.assetid: b3e6722a-25dd-4137-b224-4082e846ddec
title: KERB_SMARTCARD_CSP_INFO 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KERB_SMARTCARD_CSP_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 190c3e770a50acb7363fb10c469a7400831bc7b512d2b8158d687c83403b6df9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127338"
---
# <a name="kerb_smartcard_csp_info-structure"></a>KERB \_ 智慧卡 \_ CSP \_ 資訊結構

**KERB \_ 智慧卡 \_ CSP \_ 資訊** 結構包含智慧卡 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 的相關資訊。

未在公用標頭中宣告此結構。

## <a name="syntax"></a>語法


```C++
typedef struct _KERB_SMARTCARD_CSP_INFO {
  DWORD dwCspInfoLen;
  DWORD MessageType;
  union {
    PVOID   ContextInformation;
    ULONG64 SpaceHolderForWow64;
  };
  DWORD flags;
  DWORD KeySpec;
  ULONG nCardNameOffset;
  ULONG nReaderNameOffset;
  ULONG nContainerNameOffset;
  ULONG nCSPNameOffset;
  TCHAR bBuffer;
} KERB_SMARTCARD_CSP_INFO, *PKERB_SMARTCARD_CSP_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**dwCspInfoLen**
</dt> <dd>

此結構的大小（以位元組為單位），包括任何附加的資料。

</dd> <dt>

**MessageType**
</dt> <dd>

傳遞的訊息類型。 此成員必須設定為1。

</dd> <dt>

**CoNtextInformation**
</dt> <dd>

保留的。

</dd> <dt>

**SpaceHolderForWow64**
</dt> <dd>

保留的。

</dd> <dt>

**flags**
</dt> <dd>

保留的。

</dd> <dt>

**KeySpec**
</dt> <dd>

要從緩衝區 **bBuffer** 內指定的金鑰容器使用的私密金鑰。 索引鍵可以是下列其中一個值，定義于 WinCrypt 中。



| 值                                                                                                                                                                                                                   | 意義                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span id="AT_KEYEXCHANGE"></span><span id="at_keyexchange"></span><dl> <dt>**AT \_KEYEXCHANGE**</dt> <dt>1</dt> </dl> | 金鑰是金鑰交換金鑰。<br/> |
| <span id="AT_SIGNATURE"></span><span id="at_signature"></span><dl> <dt>**AT \_簽名**</dt> <dt>2</dt> </dl>       | 機碼是簽章金鑰。<br/>    |



 

</dd> <dt>

**nCardNameOffset**
</dt> <dd>

**BBuffer** 緩衝區中的字元數，在該緩衝區中的智慧卡名稱之前。

> [!IMPORTANT]
> 如果未提供智慧卡的名稱，緩衝區必須包含空字串。

 

</dd> <dt>

**nReaderNameOffset**
</dt> <dd>

**BBuffer** 緩衝區中的字元數，在該緩衝區中的智慧卡讀取器名稱前面。

> [!IMPORTANT]
> 如果未提供智慧卡讀卡機的名稱，則緩衝區必須包含空字串。

 

</dd> <dt>

**nContainerNameOffset**
</dt> <dd>

**BBuffer** 緩衝區中的字元數，在該緩衝區中的金鑰容器名稱之前。 這個字串不可以是空的。

</dd> <dt>

**nCSPNameOffset**
</dt> <dd>

**BBuffer** 緩衝區中的字元數，在該緩衝區中的 CSP 名稱之前。

</dd> <dt>

**bBuffer**
</dt> <dd>

初始化為長度的字元陣列 `sizeof(DWORD)` 。 此緩衝區包含 **nCardNameOffset**、 **nReaderNameOffset**、 **nContainerNameOffset** 和 **nCSPNameOffset** 成員所參考的名稱，以及 CSP 所提供的任何其他資料。

任何未提供的名稱都必須以空字串在此緩衝區中表示。

</dd> </dl>

## <a name="remarks"></a>備註

當此結構序列化時，結構成員必須對齊為2個位元組的倍數的界限。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**KERB \_ 憑證 \_ 登入**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_certificate_logon)
</dt> </dl>

 

 
