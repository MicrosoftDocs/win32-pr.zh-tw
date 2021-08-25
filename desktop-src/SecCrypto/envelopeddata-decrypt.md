---
description: 解密封裝的內容。
ms.assetid: 717d0595-e8bb-4725-bd53-fc1281cbc8ee
title: EnvelopedData 解密方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Decrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5f1c754e23977ac9c7af7f4fd3feaade13c928e9522a2285102a095fff4740b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874258"
---
# <a name="envelopeddatadecrypt-method"></a>EnvelopedData 解密方法

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。 相反地，請使用 [**EnvelopedCms 類別**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

**解密** 方法會解密已封裝的內容。 如果訊息的收件者可以存取與用來波封訊息的其中一個 [*公開金鑰*](../secgloss/p-gly.md)配對的 [*私密金鑰*](../secgloss/p-gly.md)，則會進行解密。 呼叫 **解密** 方法會重設物件的 [*狀態*](../secgloss/s-gly.md) 。 如果 **解密** 方法成功， [**EnvelopedData**](envelopeddata.md)物件的 [**Content**](envelopeddata-content.md)屬性會設定為純文字訊息。

## <a name="syntax"></a>語法


```VB
EnvelopedData.Decrypt( _
  ByVal EnvelopedMessage _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*EnvelopedMessage* \[在\]
</dt> <dd>

字串，包含要解密的封包資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

解密的資料會變成 [**EnvelopedData**](envelopeddata.md)物件的 [**Content**](envelopeddata-content.md)屬性值。

如果這個方法的使用者無法存取符合其中一個用來波封訊息之公開金鑰的私密金鑰，該方法將會失敗。 如果相關聯的私密金鑰的憑證不在 [本機電腦] 或 [目前使用者] 存放區中，則此方法將會失敗。

> [!IMPORTANT]
> 從 web 腳本呼叫這個方法時，腳本必須使用您的 [*私密金鑰*](../secgloss/p-gly.md) 來解密資料。 允許不受信任的網站使用您的私密金鑰會有安全性風險。 當第一次呼叫此方法時，會詢問網站是否可以使用您的私密金鑰的對話方塊。 如果您允許腳本使用您的私密金鑰，然後選取 [不要再詢問我]，就不會再出現任何使用您私密金鑰的腳本來解密該網域內的資料。 不過，嘗試使用私密金鑰來解密資料的網域以外的腳本仍會導致這個對話方塊出現。 如果您不允許腳本使用您的私密金鑰，然後選取 [不要再詢問我]，則該網域內的腳本將會自動拒絕使用您私密金鑰來解密資料的能力。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**加密物件**](cryptography-objects.md)
</dt> <dt>

[**EnvelopedData**](envelopeddata.md)
</dt> </dl>

 

 
