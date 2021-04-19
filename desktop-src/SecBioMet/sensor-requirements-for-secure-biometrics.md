---
title: 安全生物特徵辨識的感應器需求
description: 安全生物特徵辨識的感應器需求
ms.assetid: 6D5709E9-7B6B-4D6C-BF85-C6FB5DF5A7EE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f4e41f8300a124115c2b6cd380f904f216f491
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106966869"
---
# <a name="sensor-requirements-for-secure-biometrics"></a><span data-ttu-id="58273-103">安全生物特徵辨識的感應器需求</span><span class="sxs-lookup"><span data-stu-id="58273-103">Sensor requirements for secure biometrics</span></span>

<span data-ttu-id="58273-104">Microsoft 會利用信賴平臺模組 (TPM) 2.0，以確保在適當的硬體上，軟體 (（包括核心層級的惡意程式碼）) 如果在驗證時未提供使用者的生物特徵辨識驗證，則無法產生有效的生物特徵辨識驗證。</span><span class="sxs-lookup"><span data-stu-id="58273-104">Microsoft leverages Trusted Platform Module (TPM) 2.0 to ensure that on appropriate hardware, software (up to and including kernel-level malware) cannot produce a valid biometric authentication if the user’s biometric was not provided at the time of authentication.</span></span>

<span data-ttu-id="58273-105">若要這樣做，我們會使用 TPM 2.0 會話型授權，以及在受信任的執行環境中執行功能解壓縮和比對的感應器。</span><span class="sxs-lookup"><span data-stu-id="58273-105">To do this, we use TPM 2.0 session-based authorizations and the sensor performing feature extraction and matching in a trusted execution environment.</span></span> <span data-ttu-id="58273-106">當 Windows 生物特徵辨識架構第一次看到安全感應器功能) 所報告的安全感應器 (時，它會布建安全生物特徵辨識感應器和 TPM 之間共用的密碼。</span><span class="sxs-lookup"><span data-stu-id="58273-106">The first time the Windows Biometric Framework sees a secure sensor (as reported by the secure sensor capability), it provisions a secret that is shared between the secure biometric sensor and the TPM.</span></span> <span data-ttu-id="58273-107">該密碼永遠不會再公開給 OS，而且每個感應器都是唯一的。</span><span class="sxs-lookup"><span data-stu-id="58273-107">That secret is never again exposed to the OS, and it is unique to each sensor.</span></span>

<span data-ttu-id="58273-108">為了執行驗證，Windows 生物特徵辨識架構會開啟具有 TPM 的會話，並取得 nonce。</span><span class="sxs-lookup"><span data-stu-id="58273-108">To perform an authentication, the Windows Biometric Framework opens a session with the TPM and obtains a nonce.</span></span> <span data-ttu-id="58273-109">在安全的比對作業中，會將 nonce 傳遞到安全的感應器。</span><span class="sxs-lookup"><span data-stu-id="58273-109">The nonce is passed into the secure sensor as part of a secure match operation.</span></span> <span data-ttu-id="58273-110">感應器會在信任的執行環境中執行相符作業，如果成功，則會在該 nonce 上計算 HMAC，以及識別的使用者身分識別。</span><span class="sxs-lookup"><span data-stu-id="58273-110">The sensor performs the match in the trusted execution environment, and if it is successful, calculates an HMAC over that nonce and the identity of the user who was identified.</span></span>

<span data-ttu-id="58273-111">Windows 生物特徵辨識架構可以使用這個 HMAC，在 TPM 中為識別的使用者執行密碼編譯作業。</span><span class="sxs-lookup"><span data-stu-id="58273-111">This HMAC can be used by the Windows Biometric Framework to perform cryptographic operations in the TPM for the user who was identified.</span></span> <span data-ttu-id="58273-112">HMAC 存留期很短，在幾秒後就會到期。</span><span class="sxs-lookup"><span data-stu-id="58273-112">The HMAC is short-lived, and expires after a few seconds.</span></span>

<span data-ttu-id="58273-113">使用此通訊協定，在初始布建之後，作業系統中就不會包含任何敏感性資料。</span><span class="sxs-lookup"><span data-stu-id="58273-113">Using this protocol, after the initial provisioning, no sensitive data is contained in the OS.</span></span> <span data-ttu-id="58273-114">秘密是由 TPM 和安全感應器所持有，而在驗證期間唯一公開的是存留期為短期的 HMAC。</span><span class="sxs-lookup"><span data-stu-id="58273-114">Secrets are held by the TPM and the secure sensor, and the only thing that is exposed during the authentication is the short-lived HMAC.</span></span>

## <a name="secure-sensor-capability"></a><span data-ttu-id="58273-115">安全的感應器功能</span><span class="sxs-lookup"><span data-stu-id="58273-115">Secure sensor capability</span></span>

<span data-ttu-id="58273-116">\_ \_ \_ 如果感應器支援引擎介面卡介面 v 4.0 中的新引擎介面卡方法，則感應器必須回報 WINBIO 功能安全感應器功能。</span><span class="sxs-lookup"><span data-stu-id="58273-116">The WINBIO\_CAPABILITY\_SECURE\_SENSOR capability must be reported by the sensor if it supports the new engine adapter methods in v 4.0 of the engine adapter interface.</span></span>

<span data-ttu-id="58273-117">若要宣告感應器是安全感應器，必須符合下列需求：</span><span class="sxs-lookup"><span data-stu-id="58273-117">To claim that a sensor is a secure sensor it must meet the following requirements:</span></span>

-   <span data-ttu-id="58273-118">感應器的相符引擎必須與一般作業系統隔離 (例如，使用受信任的執行環境) </span><span class="sxs-lookup"><span data-stu-id="58273-118">The matching engine of the sensor must be isolated from the normal OS (for example, using a trusted execution environment)</span></span>
-   <span data-ttu-id="58273-119">感應器必須支援將範例的安全輸入至隔離的相符引擎;範例的內容絕不能公開給正常 OS</span><span class="sxs-lookup"><span data-stu-id="58273-119">The sensor must support secure input of samples to the isolated matching engine; the content of the samples must never be exposed to the normal OS</span></span>
-   <span data-ttu-id="58273-120">符合的引擎必須藉由執行以下所述的新 v4 方法，以支援安全的認證版本</span><span class="sxs-lookup"><span data-stu-id="58273-120">The matching engine must support secure credential release by implementing the new v4 methods outlined below</span></span>
-   <span data-ttu-id="58273-121">感應器必須支援呈現攻擊偵測。</span><span class="sxs-lookup"><span data-stu-id="58273-121">The sensor must support presentation attack detection.</span></span>

<span data-ttu-id="58273-122">WINBIO \_ 功能 \_ 安全 \_ 感應器值包含在 [**WINBIO \_ 功能**](/windows-hardware/drivers/ddi/winbio_ioctl/ns-winbio_ioctl-_winbio_sensor_attributes) 結構中。</span><span class="sxs-lookup"><span data-stu-id="58273-122">The WINBIO\_CAPABILITY\_SECURE\_SENSOR value is contained in the [**WINBIO\_CAPABILITIES**](/windows-hardware/drivers/ddi/winbio_ioctl/ns-winbio_ioctl-_winbio_sensor_attributes) structure.</span></span> <span data-ttu-id="58273-123">以下是如何定義它的範例。</span><span class="sxs-lookup"><span data-stu-id="58273-123">Here's an example of how to define it.</span></span>


```
#define WINBIO_CAPABILITY_SECURE_SENSOR     ((WINBIO_CAPABILITIES)0x00000100)
```



## <a name="error-codes"></a><span data-ttu-id="58273-124">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="58273-124">Error Codes</span></span>


```C++
//
// MessageId: WINBIO_E_INVALID_KEY_IDENTIFIER
//
// MessageText:
//
// The key identifier is invalid.
//
#define WINBIO_E_INVALID_KEY_IDENTIFIER ((HRESULT)0x80098052L)

//
// MessageId: WINBIO_E_KEY_CREATION_FAILED
//
// MessageText:
//
// The key cannot be created.
//
#define WINBIO_E_KEY_CREATION_FAILED ((HRESULT)0x80098053L)

// 
// MessageId: WINBIO_E_KEY_IDENTIFIER_BUFFER_TOO_SMALL 
//
// MessageText: 
// 
// The key identifier buffer is too small. 
// 
#define WINBIO_E_KEY_IDENTIFIER_BUFFER_TOO_SMALL ((HRESULT)0x80098054L)
```



## <a name="engine-adapter-interface-v-40"></a><span data-ttu-id="58273-125">引擎介面卡介面 v 4。0</span><span class="sxs-lookup"><span data-stu-id="58273-125">Engine adapter interface v 4.0</span></span>

<span data-ttu-id="58273-126">引擎介面卡介面版本已遞增為4.0。</span><span class="sxs-lookup"><span data-stu-id="58273-126">The engine adapter interface version has been incremented to 4.0.</span></span> <span data-ttu-id="58273-127">新介面中的額外功能可讓感應器參與 TPM 2.0。</span><span class="sxs-lookup"><span data-stu-id="58273-127">The additional functions in the new interface allow the sensor to participate in TPM 2.0.</span></span> <span data-ttu-id="58273-128">這些包括：</span><span class="sxs-lookup"><span data-stu-id="58273-128">They are:</span></span>

-   [<span data-ttu-id="58273-129">**EngineAdapterCreateKey**</span><span class="sxs-lookup"><span data-stu-id="58273-129">**EngineAdapterCreateKey**</span></span>](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_key_fn)
-   [<span data-ttu-id="58273-130">**EngineAdapterIdentifyFeatureSetSecure**</span><span class="sxs-lookup"><span data-stu-id="58273-130">**EngineAdapterIdentifyFeatureSetSecure**</span></span>](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_secure_fn)


```
// 

// Additional methods available in V4.0 and later 

// 


typedef HRESULT 

(WINAPI *PIBIO_ENGINE_CREATE_KEY_FN)( 

    _Inout_ PWINBIO_PIPELINE Pipeline, 

    _In_reads_(KeySize) const UCHAR* Key, 

    _In_ SIZE_T KeySize, 

    _Out_writes_bytes_to_(KeyIdentifierSize, *ResultSize) PUCHAR KeyIdentifier, 

    _In_ SIZE_T KeyIdentifierSize, 

    _Out_ PSIZE_T ResultSize 

    ); 


typedef HRESULT 

(WINAPI *PIBIO_ENGINE_IDENTIFY_FEATURE_SET_SECURE_FN)( 

    _Inout_ PWINBIO_PIPELINE Pipeline, 

    _In_reads_(NonceSize) const UCHAR* Nonce, 

    _In_ SIZE_T NonceSize, 

    _In_reads_(KeyIdentifierSize) const UCHAR* KeyIdentifier, 

    _In_ SIZE_T KeyIdentifierSize, 

    _Out_ PWINBIO_IDENTITY Identity, 

    _Out_ PWINBIO_BIOMETRIC_SUBTYPE SubFactor, 

 _Out_ PWINBIO_REJECT_DETAIL RejectDetail, 

    _Outptr_result_bytebuffer_(*AuthorizationSize) PUCHAR *Authorization, 

    _Out_ PSIZE_T AuthorizationSize 

    ); 


#define WINBIO_ENGINE_INTERFACE_VERSION_4   WINBIO_MAKE_INTERFACE_VERSION(4,0) 


typedef struct _WINBIO_ENGINE_INTERFACE { 

    WINBIO_ADAPTER_INTERFACE_VERSION            Version; 

    WINBIO_ADAPTER_TYPE                         Type; 

    SIZE_T                                      Size; 

    GUID                                        AdapterId; 


    PIBIO_ENGINE_ATTACH_FN                      Attach; 

    PIBIO_ENGINE_DETACH_FN                      Detach; 


    PIBIO_ENGINE_CLEAR_CONTEXT_FN               ClearContext; 


    PIBIO_ENGINE_QUERY_PREFERRED_FORMAT_FN      QueryPreferredFormat; 

    PIBIO_ENGINE_QUERY_INDEX_VECTOR_SIZE_FN     QueryIndexVectorSize; 

    PIBIO_ENGINE_QUERY_HASH_ALGORITHMS_FN       QueryHashAlgorithms; 

    PIBIO_ENGINE_SET_HASH_ALGORITHM_FN          SetHashAlgorithm; 


    PIBIO_ENGINE_QUERY_SAMPLE_HINT_FN           QuerySampleHint; 


    PIBIO_ENGINE_ACCEPT_SAMPLE_DATA_FN          AcceptSampleData;       // PROCESSES CURRENT BUFFER FROM PIPELINE AND GENERATES A FEATURE SET IN THE PIPELINE 

    PIBIO_ENGINE_EXPORT_ENGINE_DATA_FN          ExportEngineData;       // EXPORTS FEATURE SET OR TEMPLATE 


    PIBIO_ENGINE_VERIFY_FEATURE_SET_FN          VerifyFeatureSet; 

    PIBIO_ENGINE_IDENTIFY_FEATURE_SET_FN        IdentifyFeatureSet; 


    PIBIO_ENGINE_CREATE_ENROLLMENT_FN           CreateEnrollment;       // ATTACHES AN EMPTY ENROLLMENT TEMPLATE TO THE PIPELINE 

    PIBIO_ENGINE_UPDATE_ENROLLMENT_FN           UpdateEnrollment;       // CONVERTS CURRENT PIPELINE FEATURE SET INTO SOMETHING THAT CAN BE ADDED TO A TEMPLATE 

    PIBIO_ENGINE_GET_ENROLLMENT_STATUS_FN       GetEnrollmentStatus;    // QUERIES TEMPLATE ATTACHED TO THE PIPELINE TO SEE IF IT IS READY TO COMMIT 

    PIBIO_ENGINE_GET_ENROLLMENT_HASH_FN         GetEnrollmentHash; 

    PIBIO_ENGINE_CHECK_FOR_DUPLICATE_FN         CheckForDuplicate;      // DETERMINES WHETHER TEMPLATE IS ALREADY ENROLLED 

    PIBIO_ENGINE_COMMIT_ENROLLMENT_FN           CommitEnrollment; 

    PIBIO_ENGINE_DISCARD_ENROLLMENT_FN          DiscardEnrollment; 


    PIBIO_ENGINE_CONTROL_UNIT_FN                ControlUnit; 

    PIBIO_ENGINE_CONTROL_UNIT_PRIVILEGED_FN     ControlUnitPrivileged; 


#if (NTDDI_VERSION >= NTDDI_WIN8) 

    // 

    // V2.0 methods begin here... 

    // 

    PIBIO_ENGINE_NOTIFY_POWER_CHANGE_FN         NotifyPowerChange; 

    PIBIO_ENGINE_RESERVED_1_FN                  Reserved_1; 

#endif 


#if (NTDDI_VERSION >= NTDDI_WINTHRESHOLD) 

    // 

    // V3.0 methods begin here... 

    // 

    PIBIO_ENGINE_PIPELINE_INIT_FN                       PipelineInit; 

    PIBIO_ENGINE_PIPELINE_CLEANUP_FN                    PipelineCleanup; 

    PIBIO_ENGINE_ACTIVATE_FN                            Activate; 

    PIBIO_ENGINE_DEACTIVATE_FN                          Deactivate; 

    PIBIO_ENGINE_QUERY_EXTENDED_INFO_FN                 QueryExtendedInfo; 

    PIBIO_ENGINE_IDENTIFY_ALL_FN                        IdentifyAll; 

    PIBIO_ENGINE_SET_ENROLLMENT_SELECTOR_FN             SetEnrollmentSelector; 

    PIBIO_ENGINE_SET_ENROLLMENT_PARAMETERS_FN           SetEnrollmentParameters; 

    PIBIO_ENGINE_QUERY_EXTENDED_ENROLLMENT_STATUS_FN    QueryExtendedEnrollmentStatus; 

    PIBIO_ENGINE_REFRESH_CACHE_FN                       RefreshCache;  

    PIBIO_ENGINE_SELECT_CALIBRATION_FORMAT_FN           SelectCalibrationFormat; 

    PIBIO_ENGINE_QUERY_CALIBRATION_DATA_FN              QueryCalibrationData; 

    PIBIO_ENGINE_SET_ACCOUNT_POLICY_FN                  SetAccountPolicy; 

#endif 


#if (NTDDI_VERSION >= NTDDI_WIN10_RS1) 

    // 

    // V4.0 methods begin here... 

    // 

    PIBIO_ENGINE_CREATE_KEY_FN                     CreateKey; 

    PIBIO_ENGINE_IDENTIFY_FEATURE_SET_SECURE_FN    IdentifyFeatureSetSecure; 

#endif 


} WINBIO_ENGINE_INTERFACE, *PWINBIO_ENGINE_INTERFACE; 
```



## <a name="requirements"></a><span data-ttu-id="58273-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="58273-131">Requirements</span></span>

<span data-ttu-id="58273-132">Windows 10</span><span class="sxs-lookup"><span data-stu-id="58273-132">Windows 10</span></span>

 

 