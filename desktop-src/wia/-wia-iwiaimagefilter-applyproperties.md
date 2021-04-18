---
description: 可讓影像處理篩選器將屬性寫回驅動程式 (和裝置) 。
ms.assetid: b9bb8d81-2945-46ba-a0a2-7009000574aa
title: 'IWiaImageFilter：： ApplyProperties 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.ApplyProperties
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3c20527ee587b975adea34e7c480349836620015
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983503"
---
# <a name="iwiaimagefilterapplyproperties-method"></a>IWiaImageFilter：： ApplyProperties 方法

可讓影像處理篩選器將屬性寫回驅動程式 (和裝置) 。

## <a name="syntax"></a>語法


```C++
HRESULT ApplyProperties(
  [in] IWiaPropertyStorage *pWiaPropertyStorage
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pWiaPropertyStorage* \[在\]
</dt> <dd>

類型： **[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) \** _

針對要套用的屬性，指定 [_ *IWiaPropertyStorage* *](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

請勿直接從您的應用程式呼叫這個方法。 在影像處理篩選處理原始資料之後，Windows 映像取得 (WIA) 2.0 會呼叫它。

*pWiaPropertyStorage* 是影像處理篩選器應該在其中寫入屬性的 [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) 介面。 影像處理篩選器應該只使用 [IPropertyStorage：： WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) 方法來寫入屬性。

此方法可讓影像處理篩選器將屬性寫回驅動程式 (和裝置) 。 這對執行功能的篩選可能是必要的，例如在膠片掃描期間自動曝光。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia .idl</dt> </dl> |



 

 
