---
description: 要求用來連接到服務的端點。
ms.assetid: 4C02EA78-AD77-42CD-B94F-C8C3ED26CB4C
title: 'IUpdateEndpointProvider：： GetServiceEndpoint 方法 (UpdateEndpointAuth .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointProvider.GetServiceEndpoint
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: bddb77237d6d5edabab41eefe1931514fd6aed42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967155"
---
# <a name="iupdateendpointprovidergetserviceendpoint-method"></a>IUpdateEndpointProvider：： GetServiceEndpoint 方法

要求用來連接到服務的端點。

## <a name="syntax"></a>語法


```C++
HRESULT GetServiceEndpoint(
  [in]  GUID                        ServiceId,
  [in]  UpdateEndpointType          endpointType,
  [in]  UpdateEndpointProxySettings proxySettings,
  [in]  HANDLE_PTR                  hUserToken,
  [in]  BOOL                        fRefreshOnline,
  [out] BSTR                        *pbstrEndpointLoc
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ServiceId* \[在\]
</dt> <dd>

識別要更新的服務。

</dd> <dt>

*endpointType* \[在\]
</dt> <dd>

識別服務所執行的端點類型。

[**UpdateEndpointType**](updateendpointtype.md)列舉會定義下列常數。

<dt>

<span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>

<span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**


</dt> <dd>

用來連接到更新服務的用戶端伺服器端點。

</dd> <dt>

<span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>

<span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**


</dt> <dd>

當用戶端報告掃描、下載及安裝回更新服務的結果時，所使用的報表端點

</dd> <dt>

<span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>

<span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**


</dt> <dd>

當用戶端電腦連線到更新服務以查看是否有新版本的 Windows Update 代理程式用戶端軟體時，所使用的 Self-Update 端點。

</dd> <dt>

<span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>

<span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**


</dt> <dd>

當用戶端電腦聯絡規定服務，以處理適用于目的電腦的特定更新時，所使用的法規端點。

</dd> <dt>

<span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>

<span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**


</dt> <dd>

Simple-Targeting endoint，只用于 (公司環境中的 WSUS 伺服器) 的私人服務。

</dd> </dl> </dd> <dt>

*proxySettings* \[在\]
</dt> <dd>

識別連接到 proxy 伺服器時所使用的設定。

</dd> <dt>

*hUserToken* \[在\]
</dt> <dd>

包含表示使用者的 token 控制碼物件。 端點提供者會使用此權杖來決定要使用的 proxy 設定和認證。

</dd> <dt>

*fRefreshOnline* \[在\]
</dt> <dd>

表示氣象 WUA 要求新的權杖。 True 表示要求新的權杖。 False 表示要求新的或快取的標記。 如需詳細資訊，請參閱「備註」。

</dd> <dt>

*pbstrEndpointLoc* \[擴展\]
</dt> <dd>

指定用來與服務通訊的 URL。 例如，針對 cleint 伺服器端點，這會是用戶端伺服器服務的 URL。 如需詳細資訊，請參閱「備註」。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 **S \_ OK** 。 否則，會傳回 COM 或 Windows 錯誤碼。

## <a name="remarks"></a>備註

WUA 通常會在第一次呼叫此方法時，將 *fRefreshOnline* 參數設定為 false，然後如果連接錯誤時 WUA，則會在再次呼叫方法時將該參數設定為 true。 不過，此方法的執行可以從安全性權杖服務 (STS) 要求新的權杖，或隨時提供快取的權杖。

如果端點不需要驗證，則呼叫端只能使用 *pbstrEndpointLoc* 參數所指定的 URL 連接到服務。

如果端點需要驗證，則呼叫端可以使用 *pbstrEndpointLoc* 參數所指定的 URL，以及其他參數所提供的資料。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows XP、Windows 2000 專業版（含 SP3） \[ 桌面應用程式\]<br/>                   |
| 最低支援的伺服器<br/> | Windows Server 2003、Windows 2000 Server （僅含 SP3 \[ desktop 應用程式）\]<br/>                |
| 標頭<br/>                   | <dl> <dt>UpdateEndpointAuth。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>UpdateEndpointAuth .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>UpdateEndpointAuth .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IUpdateEndpointProvider**](iupdateendpointprovider.md)
</dt> </dl>

 

 




