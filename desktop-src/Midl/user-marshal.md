---
title: user_marshal 屬性
description: 使用者 \_ 封送處理 ACF 屬性會將目標 (語言中的命名區欄位型別，與在用戶端和伺服器之間傳輸 () 類型) 的傳輸類型產生關聯。
ms.assetid: a2407aa3-574d-4690-8cdf-cb1c01ca8c49
keywords:
- user_marshal 屬性 MIDL
topic_type:
- apiref
api_name:
- user_marshal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5326c9390362193a1be9dc06ee3a57f174474cc2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314797"
---
# <a name="user_marshal-attribute"></a>使用者 \_ 封送處理屬性

**使用者 \_ 封送** 處理 ACF 屬性會將目標 (語言中的命名區欄位型別，與在用戶端和伺服器之間 *傳輸 ()* *類型*) 的傳輸類型產生關聯。

``` syntax
typedef [user_marshal(userm_type)] wire-type; 
unsigned long __RPC_USER  < userm_type >_UserSize(
    unsigned long __RPC_FAR *pFlags,
    unsigned long StartingSize,
    < userm_type >  __RPC_FAR * pUser_typeObject );
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserMarshal(
    unsigned long __RPC_FAR *pFlags,
    unsigned char __RPC_FAR * Buffer,
    < userm_type >  __RPC_FAR * pUser_typeObject);
unsigned char __RPC_FAR * __RPC_USER  < userm_type >_UserUnmarshal(
    unsigned long  __RPC_FAR *  pFlags,
    unsigned char __RPC_FAR *  Buffer,
    < userm_type >  __RPC_FAR * pUser_typeObject);
void __RPC_USER  < userm_type >_UserFree(
    unsigned long  __RPC_FAR * pFlags,
    < userm_type >  __RPC_FAR * pUser_typeObject);
```

## <a name="parameters"></a>參數

<dl> <dt>

*userm-類型* 
</dt> <dd>

指定要封送處理之使用者資料類型的識別碼。 *Userm 型* 別不需要可，也不需要是 MIDL 編譯器已知的型別。

</dd> <dt>

*線路類型* 
</dt> <dd>

指定實際在用戶端與伺服器之間傳輸的命名傳輸資料類型。 網路類型必須是 MIDL 基底類型、預先定義的類型，或是可透過網路傳輸之類型的類型識別碼。

</dd> <dt>

*pFlags* 
</dt> <dd>

指定旗標欄位的指標 ( 不 [**帶正負**](unsigned.md)號的 [**長**](long.md)) 。 高序位單字會指定以 DCE 為浮點數、最大或最小的位元組和字元標記法所定義的 NDR 資料表示旗標。 低序位字組會指定封送處理內容旗標。 旗標的確切版面配置描述于 [type \_ UserSize](/windows/desktop/Rpc/the-type-usersize-function)函式中。

</dd> <dt>

*StartingSize* 
</dt> <dd>

在調整物件大小之前，指定目前的緩衝區大小 (位移) 。

</dd> <dt>

*pUser \_ typeObject* 
</dt> <dd>

指定 *userm \_ 類型* 物件的指標。

</dd> <dt>

*Buffer* 
</dt> <dd>

指定目前的緩衝區指標。

</dd> </dl>

## <a name="remarks"></a>備註

每個命名區欄位型別（ *userm*）都有一對一的對應，其 *網路類型* 會定義類型的線路標記法。 您必須提供常式來調整資料的大小以進行封送處理、封送處理和 unmarshal 資料，以及釋放記憶體。 如需這些常式的詳細資訊，請參閱 [使用者 \_ 封送處理屬性](/windows/desktop/Rpc/the-user-marshal-attribute)。 請注意，如果您的資料中也有使用 **使用者 \_ 封送** 處理或網路封送 \[ [**\[ \_ \]**](wire-marshal.md)處理來定義的內嵌類型，您也需要管理這些內嵌類型的服務。

*網路類型* 不能是介面指標或完整指標。 *網路類型* 必須有妥善定義的記憶體大小。 如需有關如何封送處理指定 *網路類型* 的詳細資訊，請參閱 [使用者 \_ 封送處理和網路 \_ 封送處理的封送處理規則](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal)。

*Userm 類型* 不應該是介面指標，因為它們可以直接封送處理。 如果使用者類型是完整的指標，您必須自行管理別名。

## <a name="examples"></a>範例

``` syntax
// Marshal a long as a structure containing two shorts.

typedef unsigned long FOUR_BYTE_DATA;
typedef struct _TWO_X_TWO_BYTE_DATA 
{ 
    unsigned short low; 
    unsigned short high; 
} TWO_X_TWO_BYTE_DATA;
```

``` syntax
// ACFL file

typedef [user_marshal(FOUR_BYTE_DATA)] TWO_X_TWO_BYTE_DATA;

// Marshaling functions:

// Calculate size that converted data will require in the buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserSize( 
    ULONG __RPC_FAR * pulFlags, 
    ULONG __RPC_FAR ulStartingSize,
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Copy FOUR_BYTE_DATA into buffer as TWO_X_TWO_BYTE_DATA
unsigned long __RPC_USER FOUR_BYTE_DATA_UserMarshal( 
    ULONG __RPC_FAR *pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Recreate FOUR_BYTE_DATA from TWO_X_TWO_BYTE_DATA in buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserUnmarshal( 
    ULONG __RPC_FAR * pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Nothing to do here as the engine frees the top node and FOUR_BYTE_DATA is a flat data type.
void __RPC_USER FOUR_BYTE_DATA_UserFree( 
    ULONG __RPC_FAR * pulFlags, 
    FOUR_BYTE_DATA __RPC_FAR * pul);
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[應用程式佈建檔 (ACF) ](application-configuration-file-acf-.md)
</dt> <dt>

[MIDL 基底類型](midl-base-types.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**表示 \_ 為**](represent-as.md)
</dt> <dt>

[**符號**](unsigned.md)
</dt> <dt>

[使用者 \_ 封送處理屬性](/windows/desktop/Rpc/the-user-marshal-attribute)
</dt> <dt>

[**網路 \_ 封送處理**](wire-marshal.md)
</dt> <dt>

[**NdrGetUserMarshalInfo**](/windows/desktop/api/rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> </dl>

 

 