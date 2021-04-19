---
title: 'IWMDRMSecurity PerformSecurityUpdate 方法 (Wmdrmsdk .h) '
description: PerformSecurityUpdate 方法會在本機電腦上起始對 DRM 子系統的安全性更新。
ms.assetid: e450a1e3-6024-4c00-9978-fbc88fde2101
keywords:
- PerformSecurityUpdate 方法 windows Media 格式
- PerformSecurityUpdate 方法 windows Media Format，IWMDRMSecurity 介面
- IWMDRMSecurity 介面 windows Media Format，PerformSecurityUpdate 方法
topic_type:
- apiref
api_name:
- IWMDRMSecurity.PerformSecurityUpdate
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a34a1e92edd279655737a2e8f3b7ce4e77e27fd5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981330"
---
# <a name="iwmdrmsecurityperformsecurityupdate-method"></a>IWMDRMSecurity：:P erformSecurityUpdate 方法

**PerformSecurityUpdate** 方法會在本機電腦上起始對 DRM 子系統的安全性更新。

## <a name="syntax"></a>語法


```C++
HRESULT PerformSecurityUpdate(
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwFlags* \[在\]
</dt> <dd>

更新選項，以下列其中一個旗標表示。



| 旗標                                          | 描述                                                                                     |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------|
| WMDRM \_ 安全性 \_ 執行 \_ INDIV               | 只有在用戶端的版本已過期時，才會將 DRM 元件設為個人化。 |
| WMDRM \_ 安全性 \_ 執行 \_ 撤銷 \_ 更新 | 會更新用戶端電腦上的撤銷清單。                               |
| WMDRM \_ 安全性 \_ 執行 \_ 強制 \_ INDIV        | 即使用戶端的版本是最新的，也會使 DRM 元件成為個人化。  |



 

</dd> <dt>

*ppunkCancelationCookie* \[擴展\]
</dt> <dd>

變數的位址，此變數會接收可用於取消此作業之物件的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

這個方法會以非同步方式執行。 它會在呼叫後立即傳回，然後根據 *dwFlags* 參數中所設定的旗標產生事件。

針對設定為 [WMDRM 安全性] 的 [ (旗標] 旗標設定為 [WMDRM \_ 安全性] \_ 執行 \_ INDIV 或 WMDRM \_ 安全性 \_ 執行 \_ 強制 \_ INDIV) ，在處理完成時，會產生一連串 **MEWMDRMIndividualizationProgress** 事件，後面接著 **MEWMDRMIndividualizationCompleted** 事件。 藉由呼叫 **IMFMediaEvent：： GetValue** 取得的每個 **MEWMDRMIndividualizationProgress** 事件的值都是 **IUnknown** 指標。 您可以呼叫所抓取 **IUnknown** 介面的 **QueryInterface** 方法，以取得 [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md)介面的實例。

若要重新整理撤銷清單 (旗標設為 [WMDRM \_ 安全性 \_ 執行撤銷重新整理) ] \_ \_ 時，會在處理完成時產生 **MEWMDRMREvocationDownloadCompleted** 事件。

> [!Note]  
> 當 **PerformSecurityUpdate** 完成個人化時，唯一會反映新的個人化狀態的現有物件就是繼承自 **IWMDRMSecurity** 的物件。 所有其他現有的物件將不會更新。 您必須釋放並重新建立任何其他物件，使其反映新的個別狀態。

 

如需使用 Windows Media DRM 用戶端擴充 Api 的非同步方法的詳細資訊，請參閱 [使用媒體基礎事件模型](using-the-media-foundation-model.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wmdrmsdk。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>Wmdrmsdk .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**自動化元件撤銷和更新**](automated-component-revocation-and-renewal.md)
</dt> <dt>

[**DRM 的個人化範例**](drm-individualization-example.md)
</dt> <dt>

[**IWMDRMSecurity 介面**](iwmdrmsecurity.md)
</dt> <dt>

[**執行 DRM 的個人化**](performing-drm-individualization.md)
</dt> </dl>

 

 





