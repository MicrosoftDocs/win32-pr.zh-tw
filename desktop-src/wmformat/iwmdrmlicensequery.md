---
title: IWMDRMLicenseQuery 介面
description: IWMDRMLicenseQuery 介面可讓應用程式查詢受保護檔案的許可權和授權狀態。
ms.assetid: 4ec8ff9f-0acb-4389-8995-65f24736491b
keywords:
- IWMDRMLicenseQuery 介面 windows 媒體格式
- IWMDRMLicenseQuery 介面 windows 媒體格式，描述
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f322a739d40f97541e6ed758f38c13d575fb42064340f006da24f31f09a07ca1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846720"
---
# <a name="iwmdrmlicensequery-interface"></a>IWMDRMLicenseQuery 介面

**IWMDRMLicenseQuery** 介面可讓應用程式查詢受保護檔案的許可權和授權狀態。 此介面會使用金鑰識別碼在本機授權存放區上執行查詢。

若要取得這個介面的實例，請呼叫 [**IWMDRMProvider：： CreateObject**](iwmdrmprovider-createobject.md)。 將 **IID \_ IWMDRMLicenseQuery** 傳遞為 *riid* 參數。

## <a name="members"></a>成員

**IWMDRMLicenseQuery** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IWMDRMLicenseQuery** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWMDRMLicenseQuery** 介面具有這些方法。



| 方法                                                                                | 描述                                                                                      |
|:--------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md)                   | 查詢本機授權存放區，以取得依金鑰識別碼執行動作的許可權。<br/>         |
| [**QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md)                     | 依金鑰識別碼和特定權利查詢本機授權存放區中的授權狀態資料。<br/> |
| [**SetActionAllowedQueryParams**](iwmdrmlicensequery-setactionallowedqueryparams.md) | 設定環境參數以改善授權查詢的精確度。<br/>             |



 

## <a name="remarks"></a>備註

**IWMDRMLicenseQuery** 方法不會提供個別授權的相關資訊。 相反地，在傳回查詢結果之前，DRM 子系統會匯總授權資料。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**介面**](drm-interfaces.md)
</dt> </dl>

 

