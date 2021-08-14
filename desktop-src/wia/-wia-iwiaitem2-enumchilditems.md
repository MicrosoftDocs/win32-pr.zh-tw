---
description: 建立列舉值物件，並將指標傳回到其 IEnumWiaItem2 介面，以取得具有 Windows 影像取得 (WIA) 2.0 裝置之 IWiaItem2 樹狀目錄中專案的資料夾。
ms.assetid: 0862bb6f-0464-491a-8cad-60b92d9609f1
title: 'IWiaItem2：： EnumChildItems 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumChildItems
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 921a6b6e85f906ef62683038b2bb28dd484d58fd20600b2ff85ae594fafb3cd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118440416"
---
# <a name="iwiaitem2enumchilditems-method"></a>IWiaItem2：： EnumChildItems 方法

建立列舉值物件，並將指標傳回到其 [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)介面，以取得具有 Windows 影像取得 (WIA) 2.0 裝置之 [**IWiaItem2**](-wia-iwiaitem2.md)樹狀目錄中專案的資料夾。

## <a name="syntax"></a>語法


```C++
HRESULT EnumChildItems(
  [in]  const GUID          *pCategoryGUID,
  [out]       IEnumWiaItem2 **ppIEnumWiaItem2
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCategoryGUID* \[在\]
</dt> <dd>

類型： **CONST GUID \***

指定要列舉其子節點的分類指標。 如果是 **Null**，則會列舉所有的子節點。

</dd> <dt>

*ppIEnumWiaItem2* \[擴展\]
</dt> <dd>

類型： **[ **IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***

接收這個方法所建立之 [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) 介面的指標位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

WIA 2.0 執行時間系統會將每個 WIA 2.0 硬體裝置表示為 [**IWiaItem2**](-wia-iwiaitem2.md) 物件的階層式樹狀結構。 **IWiaItem2：： EnumChildItems** 方法可讓應用程式列舉目前專案中的子專案。 不過，它只能套用至資料夾的專案。

如果資料夾不是空的，它就會包含 [**IWiaItem2**](-wia-iwiaitem2.md) 物件的子樹。 **IWiaItem2：： EnumChildItems** 方法會列舉資料夾中包含的所有專案。 它會在 *ppIEnumWiaItem2* 參數中儲存列舉值的指標。 應用程式會使用列舉值指標來執行物件的子專案的列舉。

應用程式必須在透過 *ppIEnumWiaItem2* 參數接收的介面指標上呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia .idl</dt> </dl> |



 

 
