---
description: Remove 方法會從開啟的憑證存放區移除憑證。 這個方法只能搭配以讀取/寫入權限開啟的存放區使用。
ms.assetid: 02bb8ff1-2240-4ec7-b8af-9a7812a12ba9
title: Store. Remove 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0f3700c8f61861987bc5311a637722955c62a1c6ad1572c7628d9ab9e0f5c76c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897683"
---
# <a name="storeremove-method"></a>Store. Remove 方法

\[**Remove** 方法可在 [需求] 區段中指定的作業系統中使用。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**system.security.cryptography.x509certificates.x509store 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1)。\]

**Remove** 方法會從開啟的 [*憑證存放區*](../secgloss/c-gly.md)移除 [*憑證*](../secgloss/c-gly.md)。 這個方法只能搭配以讀取/寫入權限開啟的存放區使用。

## <a name="syntax"></a>語法


```VB
Store.Remove( _
  ByVal Certificate _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*憑證* \[在\]
</dt> <dd>

解析為要從存放區移除的 [**憑證**](certificate.md) 物件實例的運算式。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

> [!IMPORTANT]
> 從 web 腳本呼叫這個方法時，腳本必須刪除本機電腦上的數位憑證。 允許不受信任的網站刪除數位憑證有安全性風險。 此對話方塊會詢問第一次呼叫此方法時，網站是否可以刪除憑證。 如果您允許應用程式刪除憑證，然後選取 [不要再顯示此對話方塊]，則在該網域內刪除憑證的所有腳本都不會再出現此對話方塊。 不過，嘗試刪除憑證的網域以外的腳本仍會出現此對話方塊。 如果您不允許腳本刪除憑證，然後選取 [不要再顯示此對話方塊]，則該網域內的腳本將會自動拒絕刪除憑證的能力。

 

當您從存放區刪除憑證時，您應該先刪除與憑證相關聯的私密金鑰。

如果存放區未以讀取/寫入權限開啟，這個方法將會失敗。 雖然這個方法可以與記憶體存放區搭配使用，但是在關閉存放區時，不會保存對記憶體存放區所做的任何變更。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**儲存**](store.md)
</dt> <dt>

[**加密物件**](cryptography-objects.md)
</dt> </dl>

 

 
