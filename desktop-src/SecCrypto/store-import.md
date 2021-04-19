---
description: 匯入方法會將先前匯出的憑證存放區內容複寫到開啟的憑證存放區。 這個方法只能搭配以讀取/寫入權限開啟的存放區使用。
ms.assetid: 22db8f1c-469b-4baf-9039-4da35c9c6aa0
title: Store. Import 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Import
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4eb16cc341eb6e5dcee87216a52e9e3de94d1b65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999453"
---
# <a name="storeimport-method"></a>Store. Import 方法

\[匯 **入** 方法可用於 [需求] 區段中指定的作業系統。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**system.security.cryptography.x509certificates.x509store 類別**](/previous-versions/windows/embedded/hh424027(v=msdn.10))。\]

匯 **入** 方法會將先前匯出的憑證存放區內容複寫到開啟的 [*憑證存放區*](../secgloss/c-gly.md) 。 這個方法只能搭配以讀取/寫入權限開啟的存放區使用。

## <a name="syntax"></a>語法


```VB
Store.Import( _
  ByVal EncodedStore _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*EncodedStore* \[在\]
</dt> <dd>

包含要匯入之編碼憑證的字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

> [!IMPORTANT]
> 從 web 腳本呼叫這個方法時，腳本必須存取本機電腦上的數位憑證。 如果您允許腳本存取您的數位憑證，執行腳本的網站也可以存取儲存在憑證中的任何個人資訊。 第一次從特定網域呼叫這個方法時，會產生一個對話方塊，使用者必須在此對話方塊中指出是否允許存取憑證。

 

如果存放區未以讀取/寫入權限開啟，這個方法將會失敗。 雖然這個方法可以與記憶體存放區搭配使用，但是在關閉存放區時，不會保存對記憶體存放區所做的任何變更。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**市集**](store.md)
</dt> <dt>

[**加密物件**](cryptography-objects.md)
</dt> </dl>

 

 
