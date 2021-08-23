---
title: IGatherNotify OnDataMove (已淘汰的) 方法
description: 此 Windows 桌面搜尋介面主題已被取代，並已由 Windows SDK 中的 Windows Search ISearchPersistentItemsChangedSink API 取代。 |IGatherNotify OnDataMove (已淘汰的) 方法
ms.assetid: cc223d0f-6508-4e38-b365-c60660db5324
keywords:
- OnDataMove (淘汰的) 方法舊版 Windows 環境功能
- OnDataMove (淘汰的) 方法舊版 Windows 環境功能，IGatherNotify 介面
- IGatherNotify 介面舊版 Windows 環境功能，OnDataMove (已淘汰) 方法
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataMove (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2f3d4f7d91bc9e9741f227812997a820ab4180ccf438d52ae8cfea93f67dc0bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665868"
---
# <a name="igathernotifyondatamove-deprecated-method"></a>IGatherNotify：： OnDataMove (已淘汰的) 方法

\[**OnDataMove** 可能會在作業系統或產品的後續版本中變更或無法使用。\]

此 Windows 桌面搜尋介面主題已被取代，並已由 Windows SDK 中的 Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API 取代。

這個方法會通知索引子已移動的資料。 當它將通知傳送至索引子時，它會包含舊的位址、新位址和邏輯位址。

## <a name="syntax"></a>語法


```C++
void OnDataMove (Deprecated)(
  [in] long eChangeAdviseSemantics,
  [in] BSTR bstrOldAddress,
  [in] BSTR bstrNewAddress,
  [in] BSTR bstrLogicalAddress
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*eChangeAdviseSemantics* \[在\]
</dt> <dd>

類型： **long**

列舉參數，描述發生的移動類型。

</dd> <dt>

*bstrOldAddress* \[在\]
</dt> <dd>

類型： **BSTR**

移動之專案的舊位址。 若為一般檔案，*eChangeAdviseSematics* 為 **Null**。 針對資料夾或目錄，將 *eChangeAdviseSematics* 設定為 GTHR \_ CA \_ 語義 \_ 目錄。

</dd> <dt>

*bstrNewAddress* \[在\]
</dt> <dd>

類型： **BSTR**

要移動之專案的新位址。

</dd> <dt>

*bstrLogicalAddress* \[在\]
</dt> <dd>

類型： **BSTR**

移動之專案的邏輯位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

 

 
