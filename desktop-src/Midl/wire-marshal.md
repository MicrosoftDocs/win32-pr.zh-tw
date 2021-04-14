---
title: wire_marshal 屬性
description: '\\ 電傳 \_ 封送處理 \ 屬性（attribute）會指定將用於傳輸 (類型) 的資料類型，而不是 (userm 類型) 的應用程式特定資料類型。'
ms.assetid: 51969f2c-7390-42c4-8aa6-ba12fdb22d23
keywords:
- wire_marshal 屬性 MIDL
topic_type:
- apiref
api_name:
- wire_marshal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17466648078162bc8244219f77e3ecc0dc4cb4d7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104383117"
---
# <a name="wire_marshal-attribute"></a>有線 \_ 封送處理屬性

[ **\[ 有線 \_ 封 \] 送** 處理] 屬性指定的資料類型將用於傳輸 (類型 *) ，* 而不是 (*userm 類型*) 的應用程式特定資料類型。

``` syntax
typedef [wire_marshal(wire_type)] type-specifier userm-type; 
unsigned long __RPC_USER  < userm-type >_UserSize(
    unsigned long __RPC_FAR *pFlags,
    unsigned long StartingSize,
    < userm-type > __RPC_FAR * pUser_typeObject );
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserMarshal(
    unsigned long  __RPC_FAR * pFlags,
    unsigned char __RPC_FAR * Buffer,
    < userm-type >  __RPC_FAR * pUser_typeObject);
unsigned char __RPC_FAR * __RPC_USER  < userm-type >_UserUnmarshal(
    unsigned long  __RPC_FAR *  pFlags,
    unsigned char __RPC_FAR *  Buffer,
    < userm-type > __RPC_FAR * pUser_typeObject);
void __RPC_USER  < userm-type >_UserFree(
    unsigned long  __RPC_FAR * pFlags,
    < userm-type >  __RPC_FAR * pUser_typeObject);
```

## <a name="parameters"></a>參數

<dl> <dt>

*線路類型* 
</dt> <dd>

指定實際在用戶端與伺服器之間傳輸的命名傳輸資料類型。 連線 *類型* 必須是 MIDL 基底類型、預先定義的類型，或是可透過網路傳輸之類型的類型識別碼。

</dd> <dt>

*類型規範* 
</dt> <dd>

*Userm* 類型將會成為別名的型別。

</dd> <dt>

*userm-類型* 
</dt> <dd>

指定要封送處理之使用者資料類型的識別碼。 它可以是 *類型規範* 所提供的任何類型，只要它具有妥善定義的大小即可。 *Userm 型* 別不需要可，但必須是 MIDL 編譯器的已知型別。

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

每個應用程式專屬的資料類型（ *userm 型別）* 都有 *一對一的對應，其會定義* 類型的線路標記法。 您必須提供常式來調整資料的大小以進行封送處理、封送處理和 unmarshal 資料，以及釋放記憶體。 請注意，如果您的資料中有內嵌類型也使用了 **\[ 網路 \_ 封送 \]** 處理或 **\[** [**使用者 \_ 封送**](user-marshal.md)來定義 **\]** ，則您也需要管理這些內嵌類型的服務。 如需這些常式的詳細資訊，請參閱「 [有線 \_ 封送](/windows/desktop/Rpc/the-wire-marshal-attribute)處理」屬性。

您的實作為依據憑證-DCE 規格，必須遵循封送處理規則。 您可以在中找到有關 NDR 傳送語法的詳細資料 [https://www.opengroup.org/onlinepubs/9629399/chap14.htm](https://pubs.opengroup.org/onlinepubs/9629399/chap14.htm) 。 如果您不熟悉網路通訊協定，則不建議使用 **\[ 網路 \_ 封送 \]** 處理。

*網路類型* 不能是介面指標或完整指標。 *網路類型* 必須有妥善定義的記憶體大小。 如需有關如何封送處理指定 *網路類型* 的詳細資訊，請參閱 [使用者 \_ 封送處理和網路 \_ 封送處理的封送處理規則](/windows/desktop/Rpc/marshaling-rules-for-user-marshal-and-wire-marshal)。

*Userm 類型* 不應該是介面指標，因為它們可以直接封送處理。 如果使用者類型是完整的指標，您必須自行管理別名。

您無法直接或間接使用 [ **\[ 電匯 \_ \]** ] 屬性與 [ **\[** [**配置**](allocate.md)] **\]** 屬性，因為 NDR 引擎不會控制傳輸類型的記憶體配置。

## <a name="examples"></a>範例

``` syntax
typedef unsigned long _FOUR_BYTE_DATA;

typedef struct _TWO_X_TWO_BYTE_DATA 
{
        unsigned short low;
        unsigned short high;
} TWO_X_TWO_BYTE_DATA;

typedef [wire_marshal(TWO_X_TWO_BYTE_DATA)] 
    _FOUR_BYTE_DATA FOUR_BYTE_DATA; 

//Marshaling functions:

// Calculate size that converted data will 
// require in the buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserSize( 
    ULONG __RPC_FAR * pulFlags, 
    ULONG __RPC_FAR ulStartingSize,
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Copy FOUR_BYTE_DATA into buffer as 
// TWO_X_TWO_BYTE_DATA
unsigned long __RPC_USER FOUR_BYTE_DATA_UserMarshal( 
    ULONG __RPC_FAR *pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Recreate FOUR_BYTE_DATA from TWO_X_TWO_BYTE_DATA in buffer
unsigned long __RPC_USER FOUR_BYTE_DATA_UserUnmarshal( 
    ULONG __RPC_FAR * pulFlags, 
    char __RPC_FAR * pBufferStart, 
    FOUR_BYTE_DATA __RPC_FAR * pul);

// Nothing to do here as the engine frees the top 
// node and FOUR_BYTE_DATA is a flat data type.
void __RPC_USER FOUR_BYTE_DATA_UserFree( 
    ULONG __RPC_FAR * pulFlags, 
    FOUR_BYTE_DATA __RPC_FAR * pul 
    );
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**分配**](allocate.md)
</dt> <dt>

[資料表示](/windows/desktop/Rpc/data-representation)
</dt> <dt>

[MIDL 基底類型](midl-base-types.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**NdrGetUserMarshalInfo**](/windows/desktop/api/rpcndr/nf-rpcndr-ndrgetusermarshalinfo)
</dt> <dt>

[有線 \_ 封送處理屬性](/windows/desktop/Rpc/the-wire-marshal-attribute)
</dt> <dt>

[**傳輸 \_ 為**](transmit-as.md)
</dt> <dt>

[**符號**](unsigned.md)
</dt> <dt>

[**使用者 \_ 封送處理**](user-marshal.md)
</dt> </dl>

 

 