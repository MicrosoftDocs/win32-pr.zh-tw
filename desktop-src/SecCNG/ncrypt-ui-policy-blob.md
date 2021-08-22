---
description: 與 NCRYPT \_ UI \_ 原則 \_ 屬性屬性搭配使用，以包含索引鍵的使用者介面資訊。
ms.assetid: c567d8ba-3315-4316-8e09-93b2c10a55ec
title: 'NCRYPT_UI_POLICY_BLOB 結構 (Ncrypt \_ provider .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NCRYPT_UI_POLICY_BLOB
api_type:
- HeaderDef
api_location:
- Ncrypt_provider.h
ms.openlocfilehash: 21f9f6c0f6956ffa89da45c9dcd23727c0b3cea2d4f31131713f9ed5a0c3a2fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907598"
---
# <a name="ncrypt_ui_policy_blob-structure"></a>NCRYPT \_ UI \_ 原則 \_ BLOB 結構

**NCRYPT \_ ui \_ 原則 \_ BLOB** 結構會與 [**NCRYPT \_ ui \_ 原則 \_ 屬性**](key-storage-property-identifiers.md)屬性搭配使用，以包含金鑰的使用者介面資訊。

## <a name="syntax"></a>語法


```C++
typedef struct __NCRYPT_UI_POLICY_BLOB {
  DWORD dwVersion;
  DWORD dwFlags;
  DWORD cbCreationTitle;
  DWORD cbFriendlyName;
  DWORD cbDescription;
} NCRYPT_UI_POLICY_BLOB;
```



## <a name="members"></a>成員

<dl> <dt>

**dwVersion**
</dt> <dd>

結構的版本號碼。 此成員必須包含1。

</dd> <dt>

**dwFlags**
</dt> <dd>

一組旗標，可提供額外的使用者介面資訊或需求。



| 值                                                                                                                                                                                                                                                                                                  | 意義                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="NCRYPT_UI_PROTECT_KEY_FLAG"></span><span id="ncrypt_ui_protect_key_flag"></span><dl> <dt>**NCRYPT \_UI \_ 保護 \_ 金鑰 \_ 旗**</dt>標 <dt>0x00000001</dt> </dl>                                | 視需要顯示強式金鑰使用者介面。<br/> |
| <span id="NCRYPT_UI_FORCE_HIGH_PROTECTION_FLAG"></span><span id="ncrypt_ui_force_high_protection_flag"></span><dl> <dt>**NCRYPT \_UI \_ 強制 \_ 高 \_ 保護 \_ 旗**</dt>標 <dt>0x00000002</dt> </dl> | 強制執行高保護。<br/>                           |



 

</dd> <dt>

**cbCreationTitle**
</dt> <dd>

建立標題的長度（以位元組為單位）。 建立標題是以 null 結束的 Unicode 字串，它會指定當索引鍵完成時，用來做為 [強式索引鍵] 對話方塊標題的文字。 建立標題必須緊接在 **NCRYPT \_ UI \_ 原則 \_ BLOB** 結構之後。 如果 **cbCreationTitle** 成員的值設定為0，則會使用預設建立標題作為 [強式索引鍵] 對話方塊的標題。 只有在金鑰完成時才會使用這個成員。

</dd> <dt>

**cbFriendlyName**
</dt> <dd>

金鑰的易記名稱長度（以位元組為單位）。 易記名稱是以 null 結束的 Unicode 字串，其中包含 [強式索引鍵] 對話方塊中顯示的文字作為索引鍵的名稱。 易記名稱必須緊接在此 BLOB 中的建立標題之後。 如果 **cbFriendlyName** 成員的值設定為0，就會在 [強式索引鍵] 對話方塊中使用預設名稱。 當金鑰完成和使用金鑰時，都會使用這個成員。

</dd> <dt>

**cbDescription**
</dt> <dd>

金鑰描述的長度（以位元組為單位）。 金鑰描述是以 null 結束的 Unicode 字串，其中包含 [強式索引鍵] 對話方塊中顯示的文字作為索引鍵的描述。 描述值必須緊接在此 BLOB 中的易記名稱之後。 如果 **cbDescription** 成員的值設定為0，就會在 [強式索引鍵] 對話方塊中使用預設描述。 當金鑰完成和使用金鑰時，都會使用這個成員。

</dd> </dl>

## <a name="remarks"></a>備註

此結構包含在 Ncrypt \_ 提供者 .h 標頭中。 若要使用此結構，您必須從 Microsoft 連線下載[密碼編譯提供者開發工具組](/collaborate/connect-redirect?InvitationID=CSDK-GYTG-R2PX&ProgramID=7264)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                          |
| 標頭<br/>                   | <dl> <dt>Ncrypt \_ provider。h</dt> </dl> |



 

