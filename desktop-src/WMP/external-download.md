---
title: External. 下載方法
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 下載方法會啟動一組媒體專案的下載。
ms.assetid: 10bae41c-0658-4712-8a7e-375a1ec6dc25
keywords:
- 下載方法 Windows Media Player
- 下載方法 Windows Media Player，外部類別
- 外部類別 Windows Media Player，下載方法
topic_type:
- apiref
api_name:
- External.download
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35ef0c6e6c32e8959e402080796f29a3860fe728
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995594"
---
# <a name="externaldownload-method"></a>External. 下載方法

> [!Note]  
> 本主題說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**下載** 方法會啟動一組媒體專案的下載。

## <a name="syntax"></a>語法


```JScript
External.download(
  Type,
  IDs
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*類型* \[在\]
</dt> <dd>

連結 [庫位置常數](library-location-constants.md) ，指定要下載的專案類型。 例如，CPTrackID 指定要下載一或多個曲目。

</dd> <dt>

*識別碼* \[在\]
</dt> <dd>

**字串** ，包含要下載之媒體專案的識別碼（以分號分隔）。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 11。<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**下載媒體內容**](downloading-media-content.md)
</dt> <dt>

[**類型1線上商店的外部物件**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. 購買**](external-buy.md)
</dt> <dt>

[**IWMPContentPartner：:D 下載 o)**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download)
</dt> </dl>

 

 





